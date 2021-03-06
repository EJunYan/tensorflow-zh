# Class `tensorflow::Status` <a class="md-anchor" id="AUTOGENERATED-class--tensorflow--status-"></a>





##Member Summary <a class="md-anchor" id="AUTOGENERATED-member-summary"></a>

* [`tensorflow::Status::Status()`](#tensorflow_Status_Status)
  * Create a success status.
* [`tensorflow::Status::~Status()`](#tensorflow_Status_Status)
* [`tensorflow::Status::Status(tensorflow::error::Code code, tensorflow::StringPiece msg)`](#tensorflow_Status_Status)
  * Create a status with the specified error code and msg as a human-readable string containing more detailed information.
* [`tensorflow::Status::Status(const Status &s)`](#tensorflow_Status_Status)
  * Copy the specified status.
* [`void tensorflow::Status::operator=(const Status &s)`](#void_tensorflow_Status_operator_)
* [`bool tensorflow::Status::ok() const`](#bool_tensorflow_Status_ok)
  * Returns true iff the status indicates success.
* [`tensorflow::error::Code tensorflow::Status::code() const`](#tensorflow_error_Code_tensorflow_Status_code)
* [`const string& tensorflow::Status::error_message() const`](#const_string_tensorflow_Status_error_message)
* [`bool tensorflow::Status::operator==(const Status &x) const`](#bool_tensorflow_Status_operator_)
* [`bool tensorflow::Status::operator!=(const Status &x) const`](#bool_tensorflow_Status_operator_)
* [`void tensorflow::Status::Update(const Status &new_status)`](#void_tensorflow_Status_Update)
  * If ` ok() `, stores `new_status` into `*this`. If `!ok()`, preserves the current status, but may augment with additional information about `new_status`.
* [`string tensorflow::Status::ToString() const`](#string_tensorflow_Status_ToString)
  * Return a string representation of this status suitable for printing. Returns the string `"OK"` for success.
* [`static Status tensorflow::Status::OK()`](#static_Status_tensorflow_Status_OK)

##Member Details <a class="md-anchor" id="AUTOGENERATED-member-details"></a>

#### `tensorflow::Status::Status()` <a class="md-anchor" id="tensorflow_Status_Status"></a>

Create a success status.



#### `tensorflow::Status::~Status()` <a class="md-anchor" id="tensorflow_Status_Status"></a>





#### `tensorflow::Status::Status(tensorflow::error::Code code, tensorflow::StringPiece msg)` <a class="md-anchor" id="tensorflow_Status_Status"></a>

Create a status with the specified error code and msg as a human-readable string containing more detailed information.



#### `tensorflow::Status::Status(const Status &s)` <a class="md-anchor" id="tensorflow_Status_Status"></a>

Copy the specified status.



#### `void tensorflow::Status::operator=(const Status &s)` <a class="md-anchor" id="void_tensorflow_Status_operator_"></a>





#### `bool tensorflow::Status::ok() const` <a class="md-anchor" id="bool_tensorflow_Status_ok"></a>

Returns true iff the status indicates success.



#### `tensorflow::error::Code tensorflow::Status::code() const` <a class="md-anchor" id="tensorflow_error_Code_tensorflow_Status_code"></a>





#### `const string& tensorflow::Status::error_message() const` <a class="md-anchor" id="const_string_tensorflow_Status_error_message"></a>





#### `bool tensorflow::Status::operator==(const Status &x) const` <a class="md-anchor" id="bool_tensorflow_Status_operator_"></a>





#### `bool tensorflow::Status::operator!=(const Status &x) const` <a class="md-anchor" id="bool_tensorflow_Status_operator_"></a>





#### `void tensorflow::Status::Update(const Status &new_status)` <a class="md-anchor" id="void_tensorflow_Status_Update"></a>

If ` ok() `, stores `new_status` into `*this`. If `!ok()`, preserves the current status, but may augment with additional information about `new_status`.

Convenient way of keeping track of the first error encountered. Instead of: `if (overall_status.ok()) overall_status = new_status` Use: `overall_status.Update(new_status);`

#### `string tensorflow::Status::ToString() const` <a class="md-anchor" id="string_tensorflow_Status_ToString"></a>

Return a string representation of this status suitable for printing. Returns the string `"OK"` for success.



#### `static Status tensorflow::Status::OK()` <a class="md-anchor" id="static_Status_tensorflow_Status_OK"></a>




