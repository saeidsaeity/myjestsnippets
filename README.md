# Jest Test Snippets

This repository contains Jest test snippets to help streamline your testing workflow. Each snippet is designed to facilitate writing various types of tests quickly and efficiently.

## Usage

To use these snippets, simply type the specified prefix followed by `Tab` in your test file. This will generate the corresponding test code, which you can then modify as needed.

## Snippet List

| Snippet          | Prefix       | Description                              |
|------------------|--------------|------------------------------------------|
| Mutation Test    | `mut`        | Generic mutation tests for Jest.         |
| Compare Test     | `comp`       | Generic comparison test for Jest.        |
| Type Test        | `typetest`   | Generic type test for Jest.              |
| Post Test        | `posttest`   | Test for POST requests.                  |
| Get Test         | `gettest`    | Test for GET requests.                   |
| Patch Test       | `patchtest`  | Test for PATCH requests.                 |
| Delete Test      | `deletetest` | Test for DELETE requests.                |
| Setup Jest       | `setupjest`  | Pre-configured Jest setup with common tests. |
| Async Get Test   | `agettest`   | Async test for GET requests.             |
| Async Post Test  | `aposttest`  | Async test for POST requests.            |
| Async Patch Test | `apatchtest` | Async test for PATCH requests.           |
| Async Delete Test| `adeletetest`| Async test for DELETE requests.          |

## Examples

### Mutation Test (`mut`)

```javascript
test('should be different reference to input', () => {
    const input = [];
    expect(${1:func}(input)).not.toBe(input);
});

test('should not mutate input', () => {
    const input = [];
    const copyinput = [];
    ${1:func}(input);
    expect(input).toEqual(copyinput);
});
```
### Compare Test (`comp`)
```javascript
test('should return right value', () => {
    const input = [1, 2, 3];
    const expectedOutput = [3, 2, 1];
    const output = reverseArray(input);
    expect(output).toEqual(expectedOutput);
});
```
### Type Test (typetest)
```javascript
test('should return right type', () => {
    const input = [1, 2, 3];
    expect(typeof reverseArray(input)).toBe('object');
});
```
### Post Test (posttest)
```javascript
test('POST /api/users', () => {
    const data = { name: 'John', email: 'john@example.com' };
    return request(app)
        .post('/api/users')
        .send(data)
        .expect(201)
        .then(response => {
            // assertions for response
        });
});
```
### Get Test (gettest)
``` javascript
test('GET /api/users', () => {
    return request(app)
        .get('/api/users')
        .expect(200)
        .then(response => {
            // assertions for response
        });
});
```
### Patch Test (patchtest)
``` javascript
test('PATCH /api/users/1', () => {
    const updatedData = { name: 'Updated Name' };
    return request(app)
        .patch('/api/users/1')
        .send(updatedData)
        .expect(200)
        .then(response => {
            // assertions for response
        });
});
```
### Delete Test (deletetest)
```javascript

test('DELETE /api/users/1', () => {
    return request(app)
        .delete('/api/users/1')
        .expect(204);
});
```
### Setup Jest (setupjest)
```javascript
const  = require('')
describe('    ', () => {
test('should return right type',() => {
const input = []
expect (typeof func(input) ).toBe('object')
})
test('should be different reference to input',() => {
const input = []
expect((input)).not.toBe(input);
} )
test('should not mutate input',() => {
const input = []
const copyinput = []
(input)
expect(input).toEqual(copyinput);
} )
test('should return right value',() => {
const input = []
const expectedoutput = []
const output = (input)
expect(output).toEqual(expectedoutput)
})
})
```
### Async Get Test (agettest)
```javascript
test('gets 200', async () => {
    const { body } = await request(app).get('/api/users').expect(200);
    // assertions for body
});
```
### Async Post Test (aposttest)
```javascript
test('POST 201', async () => {
    const data = { name: 'John', email: 'john@example.com' };
    const { body } = await request(app).post('/api/users').send(data).expect(201);
    // assertions for body
});
```
### Async Patch Test (apatchtest)
```javascript
test('Patch 200', async () => {
    const data = { name: 'Updated Name' };
    const { body } = await request(app).patch('/api/users/1').send(data).expect(200);
    // assertions for body
});
```
### Async Delete Test (adeletetest)
```javascript 
test('Delete 200', async () => {
    await request(app).delete('/api/users/1').expect(200);
});
```




