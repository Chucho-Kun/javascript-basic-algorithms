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




















