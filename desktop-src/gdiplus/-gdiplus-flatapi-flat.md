---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API GDI+ Flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450f89439b6ead3b8cd9a49f52a6620571f6db54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988875"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="d6ede-103">API GDI+ Flat</span><span class="sxs-lookup"><span data-stu-id="d6ede-103">GDI+ Flat API</span></span>

<span data-ttu-id="d6ede-104">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="d6ede-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="d6ede-105">As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="d6ede-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="d6ede-106">É recomendável que você não chame diretamente as funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="d6ede-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="d6ede-107">Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++.</span><span class="sxs-lookup"><span data-stu-id="d6ede-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="d6ede-108">O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="d6ede-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="d6ede-109">Como uma alternativa para os invólucros do C++, o Microsoft .NET Framework fornece um conjunto de classes wrapper de código gerenciado para GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6ede-109">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="d6ede-110">Os wrappers de código gerenciado para GDI+ pertencem aos namespaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6ede-110">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="d6ede-111">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="d6ede-111">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="d6ede-112">System. Drawing. Drawing2D</span><span class="sxs-lookup"><span data-stu-id="d6ede-112">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="d6ede-113">System. Drawing. Imaging</span><span class="sxs-lookup"><span data-stu-id="d6ede-113">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="d6ede-114">System. Drawing. Text</span><span class="sxs-lookup"><span data-stu-id="d6ede-114">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="d6ede-115">Ambos os conjuntos de wrappers (C++ e código gerenciado) usam uma abordagem orientada a objeto, portanto, há algumas diferenças entre a maneira como os parâmetros são passados para os métodos de wrapper e a maneira como os parâmetros são passados para funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="d6ede-115">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="d6ede-116">Por exemplo, um dos invólucros de C++ é a classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="d6ede-116">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="d6ede-117">Cada objeto de **matriz** tem um campo, **nativeMatrix**, que aponta para uma variável interna do tipo **GpMatrix**.</span><span class="sxs-lookup"><span data-stu-id="d6ede-117">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="d6ede-118">Quando você passa parâmetros para um método de um objeto **Matrix** , esse método passa esses parâmetros (ou um conjunto de parâmetros relacionados) junto com uma das funções na API Flat do GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6ede-118">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="d6ede-119">Mas esse método também passa o campo **nativeMatrix** (como um parâmetro de entrada) para a função de API simples.</span><span class="sxs-lookup"><span data-stu-id="d6ede-119">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="d6ede-120">O código a seguir mostra como o método [**Matrix:: distorcer**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chama a função **GdipShearMatrix ( \* matriz GpMatrix, shearX REAL, distorção real, ordem GpMatrixOrder)** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-120">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


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



<span data-ttu-id="d6ede-121">Os construtores de [**matriz**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passam o endereço de uma variável de ponteiro **GpMatrix** (como um parâmetro de saída) para a função **GdipCreateMatrix ( \* \* matriz GpMatrix)** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-121">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="d6ede-122">O **GdipCreateMatrix** cria e Inicializa uma variável **GpMatrix** interna e atribui o endereço do **GpMatrix** à variável de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="d6ede-122">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="d6ede-123">Em seguida, o construtor copia o valor do ponteiro para o campo **nativeMatrix** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-123">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


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



<span data-ttu-id="d6ede-124">Os métodos de clonagem nas classes wrapper não recebem parâmetros, mas muitas vezes passam dois parâmetros para a função subjacente na API Flat do GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6ede-124">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="d6ede-125">Por exemplo, o método [**Matrix:: clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (como um parâmetro de entrada) e o endereço de uma variável de ponteiro **GpMatrix** (como um parâmetro de saída) para a função **GdipCloneMatrix** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-125">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="d6ede-126">O código a seguir mostra como o método **Matrix:: clone** chama a função **GdipCloneMatrix ( \* matriz GpMatrix, GpMatrix \* \* cloneMatrix)** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-126">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


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



<span data-ttu-id="d6ede-127">As funções na API simples retornam um valor do tipo GpStatus.</span><span class="sxs-lookup"><span data-stu-id="d6ede-127">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="d6ede-128">A enumeração GpStatus é idêntica à enumeração de [**status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) usada pelos métodos de wrapper.</span><span class="sxs-lookup"><span data-stu-id="d6ede-128">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="d6ede-129">Em GdiplusGpStubs. h, GpStatus é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d6ede-129">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="d6ede-130">A maioria dos métodos nas classes de wrapper retorna um valor de status que indica se o método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d6ede-130">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="d6ede-131">No entanto, alguns dos métodos de wrapper retornam valores de estado.</span><span class="sxs-lookup"><span data-stu-id="d6ede-131">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="d6ede-132">Quando você chama um método wrapper que retorna um valor de estado, o método wrapper passa os parâmetros apropriados para a função subjacente na API Flat do GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6ede-132">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="d6ede-133">Por exemplo, a [**classe Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) tem um [**Método Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) que passa o campo **nativeMatrix** e o endereço de uma variável **bool** (como um parâmetro de saída) para a função **GdipIsMatrixInvertible** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-133">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="d6ede-134">O código a seguir mostra como o método **Matrix:: IsInvertible** chama a função **GdipIsMatrixInvertible (GDIPCONST GpMatrix \* matriz, \* resultado bool)** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-134">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="d6ede-135">Outro dos wrappers é a classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="d6ede-135">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="d6ede-136">Um objeto **Color** tem um único campo do tipo **ARGB**, que é definido como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="d6ede-136">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="d6ede-137">Quando você passa um objeto **Color** para um dos métodos wrapper, esse método passa o campo **ARGB** junto à função subjacente na API Flat do GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6ede-137">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="d6ede-138">O código a seguir mostra como o método [**Pen:: setColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chama a função **GdipSetPenColor (GPPEN \* Pen, ARGB ARGB)** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-138">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="d6ede-139">O método [**Color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) retorna o valor do campo **ARGB** .</span><span class="sxs-lookup"><span data-stu-id="d6ede-139">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="d6ede-140">Os tópicos a seguir mostram a relação entre a API simples do GDI+ e os métodos de invólucro do C++.</span><span class="sxs-lookup"><span data-stu-id="d6ede-140">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="d6ede-141">Funções AdjustableArrowCap</span><span class="sxs-lookup"><span data-stu-id="d6ede-141">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="d6ede-142">Funções de bitmap</span><span class="sxs-lookup"><span data-stu-id="d6ede-142">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="d6ede-143">Funções de pincel</span><span class="sxs-lookup"><span data-stu-id="d6ede-143">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="d6ede-144">Funções CachedBitmap</span><span class="sxs-lookup"><span data-stu-id="d6ede-144">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="d6ede-145">Funções CustomLineCap</span><span class="sxs-lookup"><span data-stu-id="d6ede-145">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="d6ede-146">Funções de fonte</span><span class="sxs-lookup"><span data-stu-id="d6ede-146">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="d6ede-147">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="d6ede-147">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="d6ede-148">Funções de elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="d6ede-148">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="d6ede-149">Funções GraphicsPath</span><span class="sxs-lookup"><span data-stu-id="d6ede-149">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="d6ede-150">Funções HatchBrush</span><span class="sxs-lookup"><span data-stu-id="d6ede-150">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="d6ede-151">Funções de imagem</span><span class="sxs-lookup"><span data-stu-id="d6ede-151">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="d6ede-152">Funções ImageAttributes</span><span class="sxs-lookup"><span data-stu-id="d6ede-152">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="d6ede-153">Funções LinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="d6ede-153">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="d6ede-154">Funções de matriz</span><span class="sxs-lookup"><span data-stu-id="d6ede-154">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="d6ede-155">Funções de memória</span><span class="sxs-lookup"><span data-stu-id="d6ede-155">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="d6ede-156">Funções de notificação</span><span class="sxs-lookup"><span data-stu-id="d6ede-156">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="d6ede-157">Funções PathGradientBrush</span><span class="sxs-lookup"><span data-stu-id="d6ede-157">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="d6ede-158">Funções PathIterator</span><span class="sxs-lookup"><span data-stu-id="d6ede-158">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="d6ede-159">Funções de caneta</span><span class="sxs-lookup"><span data-stu-id="d6ede-159">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="d6ede-160">Funções de região</span><span class="sxs-lookup"><span data-stu-id="d6ede-160">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="d6ede-161">Funções SolidBrush</span><span class="sxs-lookup"><span data-stu-id="d6ede-161">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="d6ede-162">Funções de formato de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d6ede-162">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="d6ede-163">Funções de texto</span><span class="sxs-lookup"><span data-stu-id="d6ede-163">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="d6ede-164">Funções de pincel de textura</span><span class="sxs-lookup"><span data-stu-id="d6ede-164">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
