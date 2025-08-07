[User role] As a senior IT Business Analyst with 20 years of experience in the construction industry, specializing in blueprint scanning systems.

[Context] This is the login screen of the system. All users must log in to use the application.

Section 1:
I will provide you with a sample template along with detailed descriptions of each item in the template. Your task is to study and remember this template. I have also included an example of a specific field in the template for your reference—please review it and learn from it.
For example: 
- 手順: Enter Email Address

I will now describe the details of the template as follows:

- No. : Display the step order number
- 手順 : Mô tả chi tiết các bước cần thực hiện trong màn hình 

Use English
Must follow the exact format of the template.
The list of fields that have been studied includes: 処理の概要,  状態, 該当項目,   呼び出し関数, 注意  according to the standard template format.
Title the table section as **"機能操作"**
Export to markdown file	

1. Read and analyze the sample template.
2. Memorize the structure and field definition rules.
3. Review some example field rows to verify correct understanding.
4. Ensure the model can recognize similar event patterns

Section 2:
I will provide you with a sample template along with detailed descriptions of each item in the template. Your task is to study and remember this template. I have also included an example of a specific field in the template for your reference—please review it and learn from it.
For example: 
- 処理の概要: Display property information in read-only format
- 状態: On initial screen
- 該当項目: -
- 呼び出し関数: -
- 注意: Field values should match DB

I will now describe the details of the template as follows:

- No. : Display the step order number
- 処理の概要: A basic description of the steps that occur when the screen is loaded.
- 状態: Describes the timing of when each step occurs. Example: Click button, On initial screen, etc.
- 該当項目: Lists the variables sent to the server.
- 呼び出し関数: For now, just enter a hyphen "-".
- 注意: Notes or remarks. If there are none, enter a hyphen "-"

Use English
Must follow the exact format of the template.
The list of fields that have been studied includes: 処理の概要,  状態, 該当項目,   呼び出し関数, 注意  according to the standard template format.
Title the table section as **"画面出力処理"**
Export to markdown file	

1. Read and analyze the sample template.
2. Memorize the structure and field definition rules.
3. Review some example field rows to verify correct understanding.
4. Ensure the model can recognize similar event patterns

Section 4:
I will provide you with a sample template along with detailed descriptions of each item in the template. Your task is to study and remember this template. I have also included an example of a specific field in the template for your reference—please review it and learn from it.	
For example:
- イベントトリガー条件: Press the キャンセル button
- 処理の概要: Cancel edit mode and revert to original state
- 重要な送信情報: なし
- 入力チェック: なし
- 処理の詳細: Discard current inputs and restore initial values
- 遷移先画面: Same screen

I will now describe the details of the template as follows:
- No. : Display the step order number
- イベントトリガー条件: Describes which button is pressed. Example: Press the キャンセル button.
- 処理の概要: A brief description of the event that occurs.
- 重要な送信情報: Lists the values send to the server.
- 入力チェック: Lists possible test cases for form validation. Example: Check required fields, Check the email exists, etc. If none, enter なし. Suggest additional 3-5 test case for actions.
- 遷移先画面: If the event ends by navigating to another screen, specify the target screen here. If not, enter Same screen.

Use English
Must follow the exact format of the template.
The list of fields that have been studied includes: イベントトリガー条件, 処理の概要, 重要な送信情報, 入力チェック, 処理の詳細 và 遷移先画面 according to the standard template format.
Title the table section as **"イベント"**
Export to markdown file	

1. Read and analyze the sample template.
2. Memorize the structure and field definition rules.
3. Review some example field rows to verify correct understanding.
4. Ensure the model can recognize similar event patterns

Section 3:
I will provide you with a sample template along with detailed descriptions of each item in the template. Your task is to study and remember this template. I have also included an example of a specific field in the template for your reference—please review it and learn from it.	
For example:
- ラベル名: Property Name
- アイテム（日本語）: 物件名 
- I/O: O
- コントロール名: Label
- 表示長: -
- 最大長: -
- 必須: -
- 有効: -
...

I will now describe the details of the template as follows:

- No. : Display the step order number
- ラベル名: Displays the English name of a field. If it cannot be translated into English, enter a hyphen ""-"".
- アイテム（日本語）: Displays the Japanese name of a field.
- I/O: If the field is a Textbox, Combobox (dropdown – but should be written as ""Combobox""), Checkbox, Radio button, or Textarea, it is considered Input. If it is a Label, then it is Output. Just write the abbreviation: use ""I"" for Input and ""O"" for Output.
- コントロール名: The type of field (Textbox, Combobox, Radio button, Image, Image button, Checkbox, Label, List, Button, Textarea, Link).
- 表示長: The display length of the text on the UI. If the field type is Input, this must have a value. Otherwise, enter ""-"". The maximum is 191 characters.
- 最大長: The maximum number of characters that can be entered into a textbox. If the field is not a textbox, enter ""-"". The maximum is 191 characters.
- 必須: Required. If the field has a red asterisk (*) on the UI, this field should have a value of ""O"", meaning input is required. Otherwise, enter ""-"".
- 有効: If the field is disabled when the page first loads, enter ""O"". Otherwise, enter ""-"".
- 属性: What kind of values can be input into the field. Current options include: Numbers, Combined data, Kana-Kanji, Half-alphanumeric symbols, Half-width numbers. If the field type (コントロール名) is Image or Label, enter ""-"". For Radio buttons, also enter ""-"".
- 文字寄せ: Alignment of the field (Left, Center, Right).
- 初期値: The initial value of the field. It can be either ""Get from DB"" or ""Blank"" depending on context. For a regular form, it's typically ""Blank"". For Edit mode, it's ""Get from DB"". For a Label, use ""Get from DB"". If it's a Button, enter ""-"".
- 入力/出力フォーマット: The format of the input value. For example, if the input is a date, the format could be ""YYYY/MM/DD"". If the field is an Image or Label, enter ""-"".
- 取得タイミング: For now, just enter ""-"".
- 注意: Used for any notes or remarks related to the corresponding field.

Use English
Must follow the exact format of the template.
The list of fields that have been studied includes: アイテム（日本語, I/O, コントロール名, 表示長, 最大長, 必須, 有効, 属性, 文字寄せ, v.v. according to the standard template format.
Title the table section as **"項目"**
Export to markdown file	

1. Read and analyze the sample template.
2. Memorize the structure and field definition rules.
3. Review some example field rows to verify correct understanding.
4. Ensure the model can recognize similar event patternsI will now describe the details of the template as follows:

Output Requirements:
- Please export a single Markdown file named: Screen_Output_Process.md
- The content should be structured as follows:
  1. Provided Image : Embed the image reference at the top of the file.
  2. The content of first section to last section
  3. Each section must follow the exact table format and content rules above
