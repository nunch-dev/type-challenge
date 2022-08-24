# Typescript Challenge Note

## Table of Contents

- [in Operator](#in-operator)
- [keyof Operator](#keyof-operator)

## in Operator

`in` 연산자는 어떠한 Property가 특정 Object에 속해있는지 확인하는데 사용.  

`n in x` 의 형태에서 `x` 가 `n` 안에 속해있는지를 확인 할 수 있다.  
이때 `x`는 Union Type을 지원한다.

javascript의 `hasOwnProperty` 에 가까운 연산자라고 볼 수 있다.

## keyof Operator

`keyof` 연산자는 해당 객체의 공개된 Property의 Union을 제공.  
`keyof T` 의 형태에서 `T`의 Property를 표기할 수 있다.

```typescript
interface Car {
  model: string;
  year: number;
}

let car: keyof Car; // 'model' | 'year' 를 제공
```

