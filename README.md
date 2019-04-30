# Eloquent Files with AWS storage S3 Bucket Config

Installation using Composer:

<code>composer require Roopchandkashyap/laravel-eloquent-files-with-aws-s3</code>


Usage: 

In your eloquent model use `\Roopchandkashyap\EloquentFiles\HasFile` trait and create a method for accessing file like below:

<pre>

&lt;?php

namespace App\Model;

use Illuminate\Database\Eloquent\Model;

class Member extends Model {

	use \Roopchandkashyap\EloquentFiles\HasFile;

	function getImageAttribute() {
		return $this->file_info("image_path");
	}

}

</pre>

Here `"image_path"` is the attribute/column name on which you want to assign the path of the uploaded file, default is "file_path".

The second argument accepted by the `file_info()` method is the array of the following options.

<table>
	<tr>
		<th>
			Name
		</td>
		<th>
			Value
		</th>
	<tr>
</table>
