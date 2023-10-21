# React Components

### Components number 1
```
const [Scrolled, setScrolled] = useState(false);
    useEffect(() => {
        const handleScroll = () => {
            if (window.scrollY > 100) { // ваш конкретный размер прокрутки
                setScrolled(true);
            } else {
                setScrolled(false);
            }
        };
        window.addEventListener('scroll', handleScroll);
        return () => {
            window.removeEventListener('scroll', handleScroll);
        };
    }, []);
```

### Components number 2
```
const [scrollY, setScrollY] = useState(0);

useEffect(() => {
    const handleScroll = () => {
      setScrollY(window.scrollY);
    };

    window.addEventListener('scroll', handleScroll);

    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
}, []);

<div className="parallax-layer" style={{ transform: `translateY(${scrollY * 0.5}px)` }}></div>
```

### Components number 3
```

```
