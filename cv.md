#Artm Moshniaga

___

__CONTACT ME:__
E-mail: artem.m89@mail.ru
VK: [artem.moshnyaga](https://vk.com/artem.moshnyaga) 
Telegram: [Art_Temka89](https://t.me/Art_Temka89) 

___

In recent years I have worked in a different specialty. I became interested in web development and decided to change my profession. 

- able to learn quickly, study and is ready to learn all the necessary development tools.
- I approach assigned tasks responsibly.

___

__SKILLS:__
JavaScript, HTML, CSS, SCSS, ReactJs (class, functional components), REST API, TypeScript, NodeJS, Redux, RTK Query, Redux Thunk, Axios, Adaptive layout, OOP

___

__CODE EXAMPLES:__


```
function sum(num1, num2) {
    const result = [];
    let lengthCounter = 1;
    let remainder = 0;
    let maxLength = Math.max(num1.length, num2.length);
    if (num1.length < num2.length) {
        num1 = "0".repeat(num2.length - num1.length) + num1;
    } else {
        num2 = "0".repeat(num1.length - num2.length) + num2;
    }
    for (let i = maxLength - 1; i >= 0; i--) {
        let sum =
            Number(num1[num1.length - lengthCounter]) +
            Number(num2[num2.length - lengthCounter]);
        if (sum < 10) {
            result.unshift(sum + remainder);
            remainder = 0;
        } else {
            result.unshift(sum - 10 + remainder);
            remainder = 1;
        }
        lengthCounter++;
    }
    return result.join("");
}
```

```
const cartSlise = createSlice({
    name: "cartSlise",
    initialState,
    reducers: {
        addItem(state, action: PayloadAction<ICartItem>) {
            const id =
                action.payload.id +
                action.payload.size +
                action.payload.type.id;
            const findItem = state.items.find((item) => item.id === id);
            if (!findItem) {
                state.items.push({ ...action.payload, count: 1, id: id });
            } else if (findItem.count < 99) {
                findItem.count++;
                findItem.price = action.payload.price * findItem.count;
            }

            state.totalPrice = calcTotalPrice(state.items);
            state.totalCount = calcTotalCount(state.items);
        },
        removeItem(state, action: PayloadAction<string>) {
            state.items = state.items.filter(
                (item) => item.id !== action.payload
            );
            state.totalPrice = calcTotalPrice(state.items);
            state.totalCount = calcTotalCount(state.items);
        },
        minusItem(state, action: PayloadAction<string>) {
            const findItem = state.items.find(
                (item) => item.id === action.payload
            );
            if (findItem && findItem.count > 1) {
                findItem.price =
                    findItem.price - findItem.price / findItem.count;
                findItem.count--;
            }
            state.totalPrice = calcTotalPrice(state.items);
            state.totalCount = calcTotalCount(state.items);
        },
        plusItem(state, action: PayloadAction<string>) {
            const findItem = state.items.find(
                (item) => item.id === action.payload
            );
            if (findItem && findItem.count < 99) {
                findItem.price =
                    findItem.price + findItem.price / findItem.count;
                findItem.count++;
            }
            state.totalPrice = calcTotalPrice(state.items);
            state.totalCount = calcTotalCount(state.items);
        },
        clearCart(state) {
            state.items = [];
            state.totalPrice = 0;
            state.totalCount = 0;
        },
    },
});

```
___
__EDUCATION:__

Secondary education.

Independently studied and trained in freely accessible online courses.

___

__ENGLISH LANGUAGE:__
A-2











