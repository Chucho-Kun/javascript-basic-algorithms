# javascript-basic-algorithms
Basic logic of algorithms in HackerRank

Original
```

function gradingStudents(grades) {
   
    let finalGrade = [];
    for(let x=0;x<grades.length;x++){
        let alumn = grades[x];
        let total = 0;
        for(let y=0;y<alumn; y += 5){
            if(alumn >= 38){
                
                let dif = Math.abs(alumn - (y + 5));
                
                if( dif < 3){
                    total = y+5;
                }else{
                    total = alumn;
                }
            }else{ 
                total = alumn 
                }
        }
        finalGrade.push(total)
    }
    
    return finalGrade;
}

let grades = [73, 67, 38, 33, 0]
gradingStudents(grades);
```
Simplyfy
```
function gradingStudents(grades) {
  return grades.map(alumn => {
    if(alumn < 38) return alumn;
    let multiplo = Math.ceil(alumn / 5)*5
    return (multiplo - alumn < 3) ? multiplo : alumn
  })   
}

let grades = [73, 67, 38, 33, 0]
gradingStudents(grades);
```
## compareTriplets

__Sample Input__
```
5 6 7
3 6 10
```
__Sample Output__
```
1 1 
```

```
function compareTriplets(a, b) {
    const tabla = a.map((x,y)=>[x,b[y]])
    
    const alice = []
    const bob = []
    
    const review = tabla.forEach((a,b)=>{
        if(a[0] > a[1]){
            alice.push(1)
        }else if( a[0] < a[1] ){
            bob.push(1)
        }
    })
    const aSum = alice.reduce((a,b)=>a+b,0);
    const bSum = bob.reduce((a,b)=>a+b,0);
    const resp = [aSum,bSum];
    
    return resp;
}

```


















