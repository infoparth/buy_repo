error: proc-macro derive panicked
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:50:1
|
50 | #[account]
| ^^^^^^^^^^
|
= help: message: Failed to get program path: NotPresent
= note: this error originates in the attribute macro `account` (in Nightly builds, run with -Z macro-backtrace for more info)

error: proc-macro derive panicked
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:146:10
|
146 | #[derive(AnchorSerialize, AnchorDeserialize, Copy, Clone, PartialEq, BorshSchema, Debug)]
| ^^^^^^^^^^^^^^^
|
= help: message: Failed to get program path: NotPresent

error[E0277]: the trait bound `TwapPrice: BorshSerialize` is not satisfied
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:70:1
|
70 | #[account]
| ^^^^^^^^^^ the trait `BorshSerialize` is not implemented for `TwapPrice`
|
note: there are multiple different versions of crate `borsh` in the dependency graph
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\borsh-0.10.4\src\ser\mod.rs:44:1
|
44 | pub trait BorshSerialize {
| ^^^^^^^^^^^^^^^^^^^^^^^^ this is the required trait
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\lib.rs:5:5
|
5 | anchor_lang::{declare_id, prelude::\*},
| -----------
| |
| one version of crate `borsh` used here, as a dependency of crate `solana_program`
| one version of crate `borsh` used here, as a dependency of crate `solana_program`
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:147:1
|
147 | pub struct TwapPrice {
| -------------------- this type doesn't implement the required trait
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\borsh-1.5.3\src\de\mod.rs:36:1
|
36 | pub trait BorshDeserialize: Sized {
| --------------------------------- this is the found trait
= help: you can use `cargo tree` to explore your dependency tree
= help: see issue #48214
= note: this error originates in the derive macro `AnchorSerialize` (in Nightly builds, run with -Z macro-backtrace for more info)
help: add `#![feature(trivial_bounds)]` to the crate attributes to enable
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\lib.rs:4:1
|
4 + #![feature(trivial_bounds)]
|

error[E0277]: the trait bound `PriceUpdateV2: BorshSerialize` is not satisfied
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:50:1
|
50 | #[account]
| ^^^^^^^^^^ the trait `BorshSerialize` is not implemented for `PriceUpdateV2`
|
note: there are multiple different versions of crate `borsh` in the dependency graph
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\borsh-0.10.4\src\ser\mod.rs:44:1
|
44 | pub trait BorshSerialize {
| ^^^^^^^^^^^^^^^^^^^^^^^^ this is the required trait
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\lib.rs:5:5
|
5 | anchor_lang::{declare_id, prelude::\*},
| -----------
| |
| one version of crate `borsh` used here, as a dependency of crate `solana_program`
| one version of crate `borsh` used here, as a dependency of crate `solana_program`
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:52:1
|
52 | pub struct PriceUpdateV2 {
| ------------------------ this type doesn't implement the required trait
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\borsh-1.5.3\src\de\mod.rs:36:1
|
36 | pub trait BorshDeserialize: Sized {
| --------------------------------- this is the found trait
= help: you can use `cargo tree` to explore your dependency tree
= note: this error originates in the attribute macro `account` (in Nightly builds, run with -Z macro-backtrace for more info)

error[E0599]: no function or associated item named `get_full_path` found for struct `TwapPrice` in the current scope
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:70:1
|
70 | #[account]
| ^^^^^^^^^^ function or associated item not found in `TwapPrice`
...
147 | pub struct TwapPrice {
| -------------------- function or associated item `get_full_path` not found for this struct
|
= help: items from traits can only be used if the trait is implemented and in scope
= note: the following trait defines an item `get_full_path`, perhaps you need to implement it:
candidate #1: `anchor_lang::IdlBuild`
= note: this error originates in the derive macro `AnchorSerialize` (in Nightly builds, run with -Z macro-backtrace for more info)

error[E0599]: no function or associated item named `create_type` found for struct `TwapPrice` in the current scope
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:70:1
|
70 | #[account]
| ^^^^^^^^^^ function or associated item not found in `TwapPrice`
...
147 | pub struct TwapPrice {
| -------------------- function or associated item `create_type` not found for this struct
|
= help: items from traits can only be used if the trait is implemented and in scope
= note: the following trait defines an item `create_type`, perhaps you need to implement it:
candidate #1: `anchor_lang::IdlBuild`
= note: this error originates in the derive macro `AnchorSerialize` (in Nightly builds, run with -Z macro-backtrace for more info)

error[E0599]: no function or associated item named `insert_types` found for struct `TwapPrice` in the current scope
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:70:1
|
70 | #[account]
| ^^^^^^^^^^ function or associated item not found in `TwapPrice`
...
147 | pub struct TwapPrice {
| -------------------- function or associated item `insert_types` not found for this struct
|
= help: items from traits can only be used if the trait is implemented and in scope
= note: the following trait defines an item `insert_types`, perhaps you need to implement it:
candidate #1: `anchor_lang::IdlBuild`
= note: this error originates in the derive macro `AnchorSerialize` (in Nightly builds, run with -Z macro-backtrace for more info)

error[E0277]: the trait bound `TwapPrice: BorshSerialize` is not satisfied
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:70:1
|
70 | #[account]
| ^^^^^^^^^^ the trait `BorshSerialize` is not implemented for `TwapPrice`
|
note: there are multiple different versions of crate `borsh` in the dependency graph
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\borsh-0.10.4\src\ser\mod.rs:44:1
|
44 | pub trait BorshSerialize {
| ^^^^^^^^^^^^^^^^^^^^^^^^ this is the required trait
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\lib.rs:5:5
|
5 | anchor_lang::{declare_id, prelude::\*},
| -----------
| |
| one version of crate `borsh` used here, as a dependency of crate `solana_program`
| one version of crate `borsh` used here, as a dependency of crate `solana_program`
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:147:1
|
147 | pub struct TwapPrice {
| -------------------- this type doesn't implement the required trait
|
::: C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\borsh-1.5.3\src\de\mod.rs:36:1
|
36 | pub trait BorshDeserialize: Sized {
| --------------------------------- this is the found trait
= help: you can use `cargo tree` to explore your dependency tree
note: required for `TwapUpdate` to implement `BorshSerialize`
--> C:\Users\parth\.cargo\registry\src\index.crates.io-1949cf8c6b5b557f\pyth-solana-receiver-sdk-0.4.0\src\price_update.rs:70:1
|
70 | #[account]
| ^^^^^^^^^^ unsatisfied trait bound introduced in this `derive` macro
71 | #[derive(BorshSchema)]
72 | pub struct TwapUpdate {
| ^^^^^^^^^^
= note: this error originates in the attribute macro `account` which comes from the expansion of the derive macro `AnchorSerialize` (in Nightly builds, run with -Z macro-backtrace for more info)

Some errors have detailed explanations: E0277, E0599.
For more information about an error, try `rustc --explain E0277`.
error: could not compile `pyth-solana-receiver-sdk` (lib) due to 8 previous errors
warning: build failed, waiting for other jobs to finish...
Error: Building IDL failed
