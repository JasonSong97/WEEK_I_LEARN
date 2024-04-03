#### coalesce

null을 0으로 바꿔주는 함수

```sql
coalesce(referee_id, 0) -- referee_id가 null인 경우 0으로 바꿔준다

-- 예시
select name from customer where coalesce(referee_id, 0) <> 2;
```