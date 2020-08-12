# myownprofiler

## How to use

```
cd $GOPATH/src/github.com/myownprofiler
go run main.go
```

- sample result
```
##  2020-08-12 17:18:37.47 +0900
  17 SELECT * FROM `categories` WHERE `id` = N
  11 SELECT * FROM `categories` WHERE `id` = ?
  10 SELECT * FROM `users` WHERE `id` = N
   4 SELECT * FROM `users` WHERE `id` = ?
   3 INSERT INTO `items` (`id`,`seller_id`,`buyer_id`,`status`,`name`,`price`,`description`,`image_name`,`category_id`,`created_at`,`updated_at`) VALUES (...S), (...S), (...S), // 省略
   2 SELECT * FROM `transaction_evidences` WHERE `item_id` = N
   1 COMMIT
   1 SELECT * FROM `users` WHERE `account_name` = ?
   1 SELECT * FROM `items` WHERE `status` IN (?,?) AND category_id IN (?, ?, ?, ?) ORDER BY created_at DESC, id DESC LIMIT ?
   1 SELECT * FROM `transaction_evidences` WHERE `item_id` = N FOR UPDATE
```
