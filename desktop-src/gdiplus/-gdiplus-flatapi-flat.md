---
description: Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. o Microsoft .NET Framework fornece um conjunto de classes de wrapper de código gerenciado para GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API GDI+ Flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee1288bdbbf86c39d201d5ccc066c1eab16cb600950edd5e848cd250e0ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977546"
---
# <a name="gdi-flat-api"></a>API GDI+ Flat

Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. as funções no GDI+ API simples são encapsuladas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente.

como uma alternativa para os invólucros do C++, o Microsoft .NET Framework fornece um conjunto de classes de wrapper de código gerenciado para GDI+. os wrappers de código gerenciado para GDI+ pertencem aos namespaces a seguir.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Ambos os conjuntos de wrappers (C++ e código gerenciado) usam uma abordagem orientada a objeto, portanto, há algumas diferenças entre a maneira como os parâmetros são passados para os métodos de wrapper e a maneira como os parâmetros são passados para funções na API simples. Por exemplo, um dos invólucros de C++ é a classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Cada objeto de **matriz** tem um campo, **nativeMatrix**, que aponta para uma variável interna do tipo **GpMatrix**. quando você passa parâmetros para um método de um objeto de **matriz** , esse método passa esses parâmetros (ou um conjunto de parâmetros relacionados) junto com uma das funções no GDI+ API simples. Mas esse método também passa o campo **nativeMatrix** (como um parâmetro de entrada) para a função de API simples. O código a seguir mostra como o método [**Matrix:: distorcer**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chama a função **GdipShearMatrix ( \* matriz GpMatrix, shearX REAL, distorção real, ordem GpMatrixOrder)** .


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



Os construtores de [**matriz**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passam o endereço de uma variável de ponteiro **GpMatrix** (como um parâmetro de saída) para a função **GdipCreateMatrix ( \* \* matriz GpMatrix)** . O **GdipCreateMatrix** cria e Inicializa uma variável **GpMatrix** interna e atribui o endereço do **GpMatrix** à variável de ponteiro. Em seguida, o construtor copia o valor do ponteiro para o campo **nativeMatrix** .


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



os métodos de clonagem nas classes wrapper não recebem parâmetros, mas geralmente passam dois parâmetros para a função subjacente na API simples GDI+. Por exemplo, o método [**Matrix:: clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (como um parâmetro de entrada) e o endereço de uma variável de ponteiro **GpMatrix** (como um parâmetro de saída) para a função **GdipCloneMatrix** . O código a seguir mostra como o método **Matrix:: clone** chama a função **GdipCloneMatrix ( \* matriz GpMatrix, GpMatrix \* \* cloneMatrix)** .


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



As funções na API simples retornam um valor do tipo GpStatus. A enumeração GpStatus é idêntica à enumeração de [**status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) usada pelos métodos de wrapper. Em GdiplusGpStubs. h, GpStatus é definido da seguinte maneira:

`typedef Status GpStatus;`

A maioria dos métodos nas classes de wrapper retorna um valor de status que indica se o método foi bem-sucedido. No entanto, alguns dos métodos de wrapper retornam valores de estado. quando você chama um método wrapper que retorna um valor de estado, o método wrapper passa os parâmetros apropriados para a função subjacente na API simples GDI+. Por exemplo, a [**classe Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) tem um [**Método Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) que passa o campo **nativeMatrix** e o endereço de uma variável **bool** (como um parâmetro de saída) para a função **GdipIsMatrixInvertible** . O código a seguir mostra como o método **Matrix:: IsInvertible** chama a função **GdipIsMatrixInvertible (GDIPCONST GpMatrix \* matriz, \* resultado bool)** .


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Outro dos wrappers é a classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Um objeto **Color** tem um único campo do tipo **ARGB**, que é definido como um **DWORD**. quando você passa um objeto **Color** para um dos métodos wrapper, esse método passa o campo **ARGB** junto à função subjacente na API simples GDI+. O código a seguir mostra como o método [**Pen:: setColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chama a função **GdipSetPenColor (GPPEN \* Pen, ARGB ARGB)** . O método [**Color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) retorna o valor do campo **ARGB** .


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



os tópicos a seguir mostram a relação entre a GDI+ API simples e os métodos de invólucro do C++.

-   [Funções AdjustableArrowCap](-gdiplus-adjustablearrowcap-flat.md)
-   [Funções de bitmap](-gdiplus-bitmap-flat.md)
-   [Funções de pincel](-gdiplus-brush-flat.md)
-   [Funções CachedBitmap](-gdiplus-cachedbitmap-flat.md)
-   [Funções CustomLineCap](-gdiplus-customlinecap-flat.md)
-   [Funções de fonte](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [Funções de elementos gráficos](-gdiplus-graphics-flat.md)
-   [Funções GraphicsPath](-gdiplus-graphicspath-flat.md)
-   [Funções HatchBrush](-gdiplus-hatchbrush-flat.md)
-   [Funções de imagem](-gdiplus-image-flat.md)
-   [Funções ImageAttributes](-gdiplus-imageattributes-flat.md)
-   [Funções LinearGradientBrush](-gdiplus-lineargradientbrush-flat.md)
-   [Funções de matriz](-gdiplus-matrix-flat.md)
-   [Funções de memória](-gdiplus-memory-flat.md)
-   [Funções de notificação](-gdiplus-notification-flat.md)
-   [Funções PathGradientBrush](-gdiplus-pathgradientbrush-flat.md)
-   [Funções PathIterator](-gdiplus-pathiterator-flat.md)
-   [Funções de caneta](-gdiplus-pen-flat.md)
-   [Funções de região](-gdiplus-region-flat.md)
-   [Funções SolidBrush](-gdiplus-solidbrush-flat.md)
-   [Funções de formato de cadeia de caracteres](-gdiplus-stringformat-flat.md)
-   [Funções de texto](-gdiplus-text-flat.md)
-   [Funções de pincel de textura](-gdiplus-texturebrush-flat.md)

 

 
