---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Microsoft .NET Framework fornece um conjunto de classes de wrapper de código gerenciado para GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API GDI+ Flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f91c3c925b7de31f27e91c70cbd1bf0cbbb2a4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394981"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="ea3cd-104">API GDI+ Flat</span><span class="sxs-lookup"><span data-stu-id="ea3cd-104">GDI+ Flat API</span></span>

<span data-ttu-id="ea3cd-105">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="ea3cd-106">As funções na API simples GDI+ são envolvidas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="ea3cd-107">É recomendável que você não chame diretamente as funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="ea3cd-108">Sempre que fizer chamadas ao GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="ea3cd-109">Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="ea3cd-110">Como alternativa aos wrappers do C++, o Microsoft .NET Framework fornece um conjunto de classes de wrapper de código gerenciado para GDI+.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-110">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="ea3cd-111">Os wrappers de código gerenciado para GDI+ pertencem aos namespaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-111">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="ea3cd-112">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="ea3cd-112">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="ea3cd-113">System.Drawing.Drawing2D</span><span class="sxs-lookup"><span data-stu-id="ea3cd-113">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="ea3cd-114">System.Drawing.Imaging</span><span class="sxs-lookup"><span data-stu-id="ea3cd-114">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="ea3cd-115">System.Drawing.Text</span><span class="sxs-lookup"><span data-stu-id="ea3cd-115">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="ea3cd-116">Ambos os conjuntos de wrappers (C++ e código gerenciado) usam uma abordagem orientada a objeto, portanto, há algumas diferenças entre a maneira como os parâmetros são passados para os métodos wrapper e a maneira como os parâmetros são passados para funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-116">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="ea3cd-117">Por exemplo, um dos wrappers do C++ é a [**classe Matrix.**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)</span><span class="sxs-lookup"><span data-stu-id="ea3cd-117">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="ea3cd-118">Cada **objeto** Matrix tem um **campo, nativeMatrix**, que aponta para uma variável interna do tipo **GpMatrix**.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-118">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="ea3cd-119">Quando você passa parâmetros para um método de um objeto **Matrix,** esse método passa esses parâmetros (ou um conjunto de parâmetros relacionados) para uma das funções na API simples GDI+.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-119">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="ea3cd-120">Mas esse método também passa o **campo nativeMatrix** (como um parâmetro de entrada) para a função de API simples.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-120">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="ea3cd-121">O código a seguir mostra como o método [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chama a função **GdipShearMatrix(GpMatrix \* matrix, REAL shearX, REAL shearY, GpMatrixOrder order).**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-121">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



<span data-ttu-id="ea3cd-122">Os [**construtores de**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Matriz passam o endereço de uma variável de ponteiro **GpMatrix** (como um parâmetro de saída) para a função **GdipCreateMatrix(GpMatrix \* \* matrix).**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-122">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="ea3cd-123">**GdipCreateMatrix** cria e inicializa uma variável **gpMatrix** interna e, em seguida, atribui o endereço do **GpMatrix** à variável de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-123">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="ea3cd-124">Em seguida, o construtor copia o valor do ponteiro para o **campo nativeMatrix.**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-124">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



<span data-ttu-id="ea3cd-125">Os métodos clone nas classes wrapper não recebem parâmetros, mas geralmente passam dois parâmetros para a função subjacente na API simples GDI+.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-125">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="ea3cd-126">Por exemplo, o método [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (como um parâmetro de entrada) e o endereço de uma variável de ponteiro **GpMatrix** (como um parâmetro de saída) para a **função GdipCloneMatrix.**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-126">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="ea3cd-127">O código a seguir mostra como o método **Matrix::Clone** chama a função **GdipCloneMatrix(GpMatrix \* matrix, GpMatrix \* \* cloneMatrix).**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-127">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



<span data-ttu-id="ea3cd-128">As funções na API simples retornam um valor do tipo GpStatus.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-128">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="ea3cd-129">A enumeração GpStatus é idêntica à [**enumeração Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) usada pelos métodos wrapper.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-129">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="ea3cd-130">Em GdiplusGpStubs.h, GpStatus é definido da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="ea3cd-130">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="ea3cd-131">A maioria dos métodos nas classes wrapper retorna um valor de status que indica se o método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-131">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="ea3cd-132">No entanto, alguns dos métodos wrapper retornam valores de estado.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-132">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="ea3cd-133">Quando você chama um método wrapper que retorna um valor de estado, o método wrapper passa os parâmetros apropriados para a função subjacente na API simples GDI+.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-133">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="ea3cd-134">Por exemplo, a classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) tem um método [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) que passa o campo **nativeMatrix** e o endereço de uma **variável BOOL** (como um parâmetro de saída) para a **função GdipIsMatrixInvertible.**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-134">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="ea3cd-135">O código a seguir mostra como o método **Matrix::IsInvertible** chama a função **GdipIsMatrixInvertible(GDIPCONST GpMatrix \* matrix, BOOL \* result).**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-135">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="ea3cd-136">Outro dos wrappers é a [**classe**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Color.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-136">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="ea3cd-137">Um **objeto Color** tem um único campo do tipo **ARGB,** que é definido como um **DWORD.**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-137">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="ea3cd-138">Quando você passa um objeto **Color** para um dos métodos wrapper, esse método passa o campo **ARGB** para a função subjacente na API plana GDI+.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-138">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="ea3cd-139">O código a seguir mostra como o [**método Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chama a função **GdipSetPenColor(gpPen \* pen, ARGB argb).**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-139">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="ea3cd-140">O [**método Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) retorna o valor do **campo ARGB.**</span><span class="sxs-lookup"><span data-stu-id="ea3cd-140">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="ea3cd-141">Os tópicos a seguir mostram a relação entre a API simples GDI+ e os métodos de wrapper do C++.</span><span class="sxs-lookup"><span data-stu-id="ea3cd-141">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="ea3cd-142">Funções AdjustableArrowCap</span><span class="sxs-lookup"><span data-stu-id="ea3cd-142">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="ea3cd-143">Funções bitmap</span><span class="sxs-lookup"><span data-stu-id="ea3cd-143">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="ea3cd-144">Funções de pincel</span><span class="sxs-lookup"><span data-stu-id="ea3cd-144">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="ea3cd-145">Funções CachedBitmap</span><span class="sxs-lookup"><span data-stu-id="ea3cd-145">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="ea3cd-146">Funções CustomLineCap</span><span class="sxs-lookup"><span data-stu-id="ea3cd-146">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="ea3cd-147">Funções de fonte</span><span class="sxs-lookup"><span data-stu-id="ea3cd-147">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="ea3cd-148">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="ea3cd-148">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="ea3cd-149">Funções de elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="ea3cd-149">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="ea3cd-150">Funções GraphicsPath</span><span class="sxs-lookup"><span data-stu-id="ea3cd-150">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="ea3cd-151">Funções Do HatchBrush</span><span class="sxs-lookup"><span data-stu-id="ea3cd-151">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="ea3cd-152">Funções de imagem</span><span class="sxs-lookup"><span data-stu-id="ea3cd-152">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="ea3cd-153">Funções ImageAttributes</span><span class="sxs-lookup"><span data-stu-id="ea3cd-153">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="ea3cd-154">Funções LinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="ea3cd-154">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="ea3cd-155">Funções de matriz</span><span class="sxs-lookup"><span data-stu-id="ea3cd-155">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="ea3cd-156">Funções de memória</span><span class="sxs-lookup"><span data-stu-id="ea3cd-156">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="ea3cd-157">Funções de notificação</span><span class="sxs-lookup"><span data-stu-id="ea3cd-157">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="ea3cd-158">Funções PathGradientBrush</span><span class="sxs-lookup"><span data-stu-id="ea3cd-158">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="ea3cd-159">Funções PathIterator</span><span class="sxs-lookup"><span data-stu-id="ea3cd-159">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="ea3cd-160">Funções de caneta</span><span class="sxs-lookup"><span data-stu-id="ea3cd-160">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="ea3cd-161">Funções de região</span><span class="sxs-lookup"><span data-stu-id="ea3cd-161">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="ea3cd-162">Funções SolidBrush</span><span class="sxs-lookup"><span data-stu-id="ea3cd-162">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="ea3cd-163">Funções de formato de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="ea3cd-163">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="ea3cd-164">Funções de texto</span><span class="sxs-lookup"><span data-stu-id="ea3cd-164">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="ea3cd-165">Funções de pincel de textura</span><span class="sxs-lookup"><span data-stu-id="ea3cd-165">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
