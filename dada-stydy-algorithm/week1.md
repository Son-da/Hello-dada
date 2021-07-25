# 프로그래머스 - K번째 수

```javascript

// i, j, k 임의 추출
// i~j 슬라이스
// 슬라이스 한값 오른차순 정렬
// 정렬한 숫자 중 3번째 추출(answer)

// array를 for문으로 크게돌려

// commands 안에 253을 어떻게 찝을지(3번돌리기 위해 for문(length 50)), 슬라이스 > 정렬> k만큼



function solution(array, commands) {
    const answer = [];
    for (let i =0; i<commands.length; i++){
        let arr= array.slice(commands[i][0]-1 , commands[i][1])
        arr.sort(function( a,b){
            return a-b;
        } );
        answer.push(arr[commands[i][2] -1]);
    }
        
    
    return answer;
}


```
