<p align="center"><br><img src="https://user-images.githubusercontent.com/236501/85893648-1c92e880-b7a8-11ea-926d-95355b8175c7.png" width="128" height="128" /></p>
<h2 align="center">API DB CONNECTION DOCUMENTATION</h2>
<p align="center"><strong><code>@capacitor-community/sqlite</code></strong></p>
<p align="center">
  SQLite DB Connection Wrapper</p>

## Methods Index

<docgen-index>

* [`getConnectionDBName()`](#getconnectiondbname)
* [`open()`](#open)
* [`close()`](#close)
* [`execute(...)`](#execute)
* [`query(...)`](#query)
* [`run(...)`](#run)
* [`executeSet(...)`](#executeset)
* [`isExists()`](#isexists)
* [`delete()`](#delete)
* [`createSyncTable()`](#createsynctable)
* [`setSyncDate(...)`](#setsyncdate)
* [`getSyncDate()`](#getsyncdate)
* [`exportToJson(...)`](#exporttojson)
* [Interfaces](#interfaces)

</docgen-index>

## API DB Connection Wrapper

<docgen-api class="custom-css">
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

SQLiteDBConnection Interface

### getConnectionDBName()

```typescript
getConnectionDBName() => string
```

Get SQLite DB Connection DB name

**Returns:** <code>string</code>

**Since:** 2.9.0 refactor

--------------------


### open()

```typescript
open() => Promise<void>
```

Open a SQLite DB Connection

**Since:** 2.9.0 refactor

--------------------


### close()

```typescript
close() => Promise<void>
```

Close a SQLite DB Connection

**Since:** 2.9.0 refactor

--------------------


### execute(...)

```typescript
execute(statements: string) => Promise<capSQLiteChanges>
```

Execute SQLite DB Connection Statements

| Param            | Type                |
| ---------------- | ------------------- |
| **`statements`** | <code>string</code> |

**Returns:** <code>Promise&lt;<a href="#capsqlitechanges">capSQLiteChanges</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### query(...)

```typescript
query(statement: string, values?: string[] | undefined) => Promise<capSQLiteValues>
```

Execute SQLite DB Connection Query

| Param           | Type                  | Description |
| --------------- | --------------------- | ----------- |
| **`statement`** | <code>string</code>   |             |
| **`values`**    | <code>string[]</code> | (optional)  |

**Returns:** <code>Promise&lt;<a href="#capsqlitevalues">capSQLiteValues</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### run(...)

```typescript
run(statement: string, values?: any[] | undefined) => Promise<capSQLiteChanges>
```

Execute SQLite DB Connection Raw Statement

| Param           | Type                | Description |
| --------------- | ------------------- | ----------- |
| **`statement`** | <code>string</code> |             |
| **`values`**    | <code>any[]</code>  | (optional)  |

**Returns:** <code>Promise&lt;<a href="#capsqlitechanges">capSQLiteChanges</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### executeSet(...)

```typescript
executeSet(set: capSQLiteSet[]) => Promise<capSQLiteChanges>
```

Execute SQLite DB Connection Set

| Param     | Type                        |
| --------- | --------------------------- |
| **`set`** | <code>capSQLiteSet[]</code> |

**Returns:** <code>Promise&lt;<a href="#capsqlitechanges">capSQLiteChanges</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### isExists()

```typescript
isExists() => Promise<capSQLiteResult>
```

Check if a SQLite DB Connection exists

**Returns:** <code>Promise&lt;<a href="#capsqliteresult">capSQLiteResult</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### delete()

```typescript
delete() => Promise<void>
```

Delete a SQLite DB Connection

**Since:** 2.9.0 refactor

--------------------


### createSyncTable()

```typescript
createSyncTable() => Promise<capSQLiteChanges>
```

Create a synchronization table

**Returns:** <code>Promise&lt;<a href="#capsqlitechanges">capSQLiteChanges</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### setSyncDate(...)

```typescript
setSyncDate(syncdate: string) => Promise<void>
```

Set the synchronization date

| Param          | Type                |
| -------------- | ------------------- |
| **`syncdate`** | <code>string</code> |

**Since:** 2.9.0 refactor

--------------------


### getSyncDate()

```typescript
getSyncDate() => Promise<capSQLiteSyncDate>
```

Get the synchronization date

**Returns:** <code>Promise&lt;<a href="#capsqlitesyncdate">capSQLiteSyncDate</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### exportToJson(...)

```typescript
exportToJson(mode: string) => Promise<capSQLiteJson>
```

Export the given database to a JSON Object

| Param      | Type                |
| ---------- | ------------------- |
| **`mode`** | <code>string</code> |

**Returns:** <code>Promise&lt;<a href="#capsqlitejson">capSQLiteJson</a>&gt;</code>

**Since:** 2.9.0 refactor

--------------------


### Interfaces


#### capSQLiteChanges

| Prop          | Type                                        | Description                               |
| ------------- | ------------------------------------------- | ----------------------------------------- |
| **`changes`** | <code><a href="#changes">Changes</a></code> | a returned <a href="#changes">Changes</a> |


#### Changes

| Prop          | Type                | Description                                          |
| ------------- | ------------------- | ---------------------------------------------------- |
| **`changes`** | <code>number</code> | the number of changes from an execute or run command |
| **`lastId`**  | <code>number</code> | the lastId created from a run command                |


#### capSQLiteValues

| Prop         | Type               | Description                      |
| ------------ | ------------------ | -------------------------------- |
| **`values`** | <code>any[]</code> | the data values list as an Array |


#### capSQLiteSet

| Prop            | Type                | Description                      |
| --------------- | ------------------- | -------------------------------- |
| **`statement`** | <code>string</code> | A statement                      |
| **`values`**    | <code>any[]</code>  | the data values list as an Array |


#### capSQLiteResult

| Prop         | Type                 | Description                                   |
| ------------ | -------------------- | --------------------------------------------- |
| **`result`** | <code>boolean</code> | result set to true when successful else false |


#### capSQLiteSyncDate

| Prop           | Type                | Description              |
| -------------- | ------------------- | ------------------------ |
| **`syncDate`** | <code>number</code> | the synchronization date |


#### capSQLiteJson

| Prop         | Type                                              | Description           |
| ------------ | ------------------------------------------------- | --------------------- |
| **`export`** | <code><a href="#jsonsqlite">JsonSQLite</a></code> | an export JSON object |


#### JsonSQLite

| Prop            | Type                     | Description                                           |
| --------------- | ------------------------ | ----------------------------------------------------- |
| **`database`**  | <code>string</code>      | The database name                                     |
| **`version`**   | <code>number</code>      | The database version                                  |
| **`encrypted`** | <code>boolean</code>     | Set to true (database encryption) / false             |
| **`mode`**      | <code>string</code>      | * Set the mode ["full", "partial"]                    |
| **`tables`**    | <code>JsonTable[]</code> | * Array of Table (<a href="#jsontable">JsonTable</a>) |


#### JsonTable

| Prop          | Type                      | Description                                              |
| ------------- | ------------------------- | -------------------------------------------------------- |
| **`name`**    | <code>string</code>       | The database name                                        |
| **`schema`**  | <code>JsonColumn[]</code> | * Array of Schema (<a href="#jsoncolumn">JsonColumn</a>) |
| **`indexes`** | <code>JsonIndex[]</code>  | * Array of Index (<a href="#jsonindex">JsonIndex</a>)    |
| **`values`**  | <code>any[][]</code>      | * Array of Table data                                    |


#### JsonColumn

| Prop             | Type                | Description                         |
| ---------------- | ------------------- | ----------------------------------- |
| **`column`**     | <code>string</code> | The column name                     |
| **`value`**      | <code>string</code> | The column data (type, unique, ...) |
| **`foreignkey`** | <code>string</code> | The column foreign key constraints  |


#### JsonIndex

| Prop        | Type                | Description                                                                                                             |
| ----------- | ------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **`name`**  | <code>string</code> | The index name                                                                                                          |
| **`value`** | <code>string</code> | The value of the index can have the following formats: email email ASC email, MobileNumber email ASC, MobileNumber DESC |
| **`mode`**  | <code>string</code> | the mode (Optional) UNIQUE                                                                                              |

</docgen-api>