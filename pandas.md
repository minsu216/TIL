# merge 함수 예제
![merge 예제](aseets\cap.png)
![merge 예제2](aseets\cap2.png)

# join 함수 
```python
left1.join(right1, on='key)
#left1의 key열을 기준으로 매핑됨

left1.join([right1,another] on='key)
#join할 때 다른 데이터도 같이 넣을 수 있다.
```

# np.concatenate 함수
```python
arr = np.arange(12).reshape((3, 4))
# array([[ 0,  1,  2,  3],
#        [ 4,  5,  6,  7],
#        [ 8,  9, 10, 11]])

np.concatenate([arr,arr]) #위아래
# array([[ 0,  1,  2,  3],
#        [ 4,  5,  6,  7],
#        [ 8,  9, 10, 11],
#        [ 0,  1,  2,  3],
#        [ 4,  5,  6,  7],
#        [ 8,  9, 10, 11]])
np.concatenate([arr,arr],axis=1) #좌우 
# array([[ 0,  1,  2,  3,  0,  1,  2,  3],
#        [ 4,  5,  6,  7,  4,  5,  6,  7],
#        [ 8,  9, 10, 11,  8,  9, 10, 11]])

#* 열의 개수가 같아야 axis =1 이 성립되고
#* 행의 개수가 같아야 axis =0 이 성립이된다.
```

