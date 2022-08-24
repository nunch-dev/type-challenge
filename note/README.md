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

## @ts-expect-error

`@ts-ignore` 처럼 타입에러가 발생하는 부분을 무시하는 기능을 하나 근본적으로 다름

- `타입스크립트 에러가 발생할 것을 안다` 가 전제 
  - 그럼에도 불구하고 에러를 무시해야 한다.
- 런타임 에러가 발생하면 안된다. 타입 에러일 경우에만 허용

궁극적으로는 에러가 발생하는 구문을 테스트 하기 위해 사용하는 주석이라고 생각하면 좋다

[참고](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-3-9.html#-ts-expect-error-comments)

