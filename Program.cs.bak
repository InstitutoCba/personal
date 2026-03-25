var builder = WebApplication.CreateBuilder(args);

// Add services to the container.
builder.Services.AddRazorPages();

var app = builder.Build();

// Configure the HTTP request pipeline.
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Error");
    app.UseHsts();
}

app.UseHttpsRedirection();

// Servir archivos estáticos (IMPORTANTE: Esto debe ir ANTES del routing)
app.UseDefaultFiles(); // Sirve index.html como página principal
app.UseStaticFiles();  // Sirve archivos estáticos (HTML, CSS, imágenes)

app.UseRouting();

app.UseAuthorization();

app.MapStaticAssets();
app.MapRazorPages()
   .WithStaticAssets();

app.Run();
