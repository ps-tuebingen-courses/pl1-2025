```racket
(reset (list (+ (one-of (list 1 2 3)) (one-of (list 9 12 154))))))
```

-->

```racket
(reset (list (+ (shift k (apply append (map (lambda (x) (k x)) (list 1 2 3)))) (one-of (list 9 12 154)))))
```

-->

```racket
(reset (apply append (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 1 2 3))))
```

-->

```racket
(reset (apply append (cons (reset (list (+ 1 (one-of (list 9 12 154))))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (reset (list (+ 1 (shift k (apply append (map (lambda (x) (k x)) (list 9 12 154))))))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (reset (apply append (map (lambda (x) (reset (list (+ 1 x)))) (list 9 12 154)))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (reset (apply append (list (reset (list 10)) (reset (list 13)) (reset (list 155))))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (reset (apply append (list (list 10) (list 13) (list 155)))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (reset (list 10 13 155)) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 2 3)))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (reset (list (+ 2 (one-of (list 9 12 154))))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 3))))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (reset (apply append (map (lambda (x) (reset (list (+ 2 x)))) (list 9 12 154)))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 3))))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (list 11 14 156) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) (list 3))))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (list 11 14 156) (cons (reset (list (+ 3 (one-of (list 9 12 154))))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) empty))))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (list 11 14 156) (cons (reset (apply append (map (lambda (x) (reset (list (+ 3 x)))) (list 9 12 154)))) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) empty))))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (list 11 14 156) (cons (list 12 15 157) (map (lambda (x) (reset (list (+ x (one-of (list 9 12 154)))))) empty))))))
```

-->

```racket
(reset (apply append (cons (list 10 13 155) (cons (list 11 14 156) (cons (list 12 15 157) empty)))))
```

-->

```racket
(reset (list 10 13 155 11 14 156 12 15 157))
```

-->

```racket
(list 10 13 155 11 14 156 12 15 157)
```
