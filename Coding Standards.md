## <h1 dir='rtl'> استاندارهای کدنویسی:</h1>

<h2 dir='rtl'>کامنت‌گذاری:</h2>

<p dir='rtl'>
در تعریف کلاس‌ها، متدها حتما بشکل زیر توضیحات اضافه شوند، جهت دسترسی کافی است قبل از تعریف متد از /// و کلید tab استفاده شود و سپس موارد مورد نیاز تکمیل شود.
</p>
>
>	/// <summary>
>	/// Service responsible for Handling Database Connection
>	/// </summary>
>	public class DataService
>	{
>		/// <summary>	
>		/// Check if Database Connection is Valid
>		/// </summary>
>		public bool IsValid;
>		/// <summary>
>		/// set Connection String of Database
>		/// </summary>
>		/// <param name="connectionString"> Connection String  should contain
>		///Database server and username and password </param>
>		public void SetDatabaseConnection(string connectionString)
>		{}
>	}
<p dir='rtl'>
در کامنت گذاری برای Api ها حتما، نمونه Sample هم جزو کامنت طبق استاندارد قرار بگیرد.  
    برای نمونه از لینک زیر استفاده کنید
</p>
[getting-started-with-swashbuckle](https://docs.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-5.0&tabs=visual-studio)
---
<h2 dir='rtl'>نام گذاری</h2>
<p dir='rtl'>
نام متغیرها، متدها، اینترفیس‌ها، کلاس‌ها و ... باید بدرستی انتخاب شود. نام انتخابی باید معنی کاری که قرار است انجام شود را داشته باشد. 
<br>
استفاده از اختصار در نام‌گذاری‌ها تا حد امکان پرهیز شود.
</p>
<h4 dir="rtl">نام‌گذاری Class و Struct بشکل PascalCasing باشد.</h4>
>	
>	public class DataService
>	{
>	}

<h4 dir="rtl">نام‌گذاری Interface بشکل PascalCasing با اضافه‌کردن I در ابتدای نام باشد.</h4>
>
>	public interface IDataService
>	{
>	}

<h4 dir="rtl">نام‌گذاری متدها و property هایی که بشکل public هستند بشکل PascalCasing باشند.</h4>
>
>	public class DataService
>	{
>		bool IsValid;
>		void GetDatabaseConnection()
>		{
>		}
>	}

<h4 dir="rtl">نام‌گذاری property هایی که بشکل private هستند بشکل camelCasing باشد. </h4>
<h4 dir="rtl">برای استفاده از Interface ها یا Context ابتدای نام _ استفاده شود.</h4>
>	
>	public class DataService
>	{
>		private IWorkerQueue _workerQueue;
>	}

<h4 dir="rtl">نام‌گذاری پارامترها، متغیرهای محلی بشکل camelCasing باشد.</h4>
>
>	public T SomeMethod<T>(int someNumber, bool isValid)
>	{
>	}

<h2 dir="rtl">Layout</h2>
<ol dir="rtl">
	<li>در هر خط از کد یک دستور نوشته شود.</li>
	<li>در هر خط یک تعریف انجام شود.</li>
    <li>بلوک‌های کد که در یک بلوک دیگر تعریف می‌شود از ابتدای بلوک به اندازه یک tab فاصله داشته باشد</li>
	<li>برای دستورات If یا For که یک دستور را انجام می‌دهند هم از {} برای مشخص کردن بلوک کد استفاده شود.</li>
</ol>

<h2 dir="rtl">Language Specific</h2>
<ul dir="rtl">
	<li>در استفاده از نوع‌های ابتدایی مثل int,string از معادل .net (Int,String) استفاده نشود.</li>
	<li>برای ساخت string از متغیرها یا از تابع format استفاده شود یا از $ استفاده گردد.</li>
</ul>

>
>    string displayName = $"{nameList[n].LastName}, {nameList[n].FirstName}";

>
>    string displayName = string.Format("{0} , {1}", nameList[n].LastName, nameList[n]. FirstName);

<h4 dir="rtl">استفاده از var برای نوع متغیر فقط در صورتی استفاده شود که از سمت راست نوع مشخص باشد یا نوع اهمیت نداشته باشد.</h4>
<h5 dir="rtl">در حلقه‌های foreach بهتر است از Var استفاده نشود.</h5>
>
>	foreach (char ch in laugh)
>	{
>		if (ch == 'h')
>		{
>			Console.Write("H");
>		}
>		else
>		{
>			Console.Write(ch);
>		}
>	}

<h4 dir="rtl">در دستورات مقایسه‌ای به منظور افزایش کارایی کد، از && و ||  بجای & و | استفاده شود</h4>
<h4 dir="rtl">در هنگام نمونه سازی از یک کلاس بشکل زیر عمل شود.</h4>
>
>	var instance1 = new ExampleClass();
>
>
>	var instance3 = new ExampleClass 
>		{ 
>		Name = "Desktop",
>		ID = 37414,
>		Location = "Redmond", 
>		Age = 2.3 
>		};

<h2 dir="rtl">جهت مطالعه بیشتر به لینک های زیر مراجعه کنید.</h4>

https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions

https://github.com/ktaranov/naming-convention/blob/master/C%23%20Coding%20Standards%20and%20Naming%20Conventions.md
