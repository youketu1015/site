# operator=
* iterator[meta header]
* std[meta namespace]
* front_insert_iterator[meta class]
* function[meta id-type]

```cpp
front_insert_iterator&
  operator=(const typename Container::value_type& value); // (1) C++03
constexpr front_insert_iterator&
  operator=(const typename Container::value_type& value); // (1) C++20

front_insert_iterator&
  operator=(typename Container::value_type&& value);      // (2) C++11
constexpr front_insert_iterator&
  operator=(typename Container::value_type&& value);      // (2) C++20
```

## 概要
値を出力する


## 効果
- `const`参照版：`container->push_front(value);`
- 右辺値参照版： `container->push_front(`[`std::move`](/reference/utility/move.md)`(value));`


## 戻り値
`*this`


## 参照
- [P1032R1 Misc `constexpr` bits](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1032r1.html)
