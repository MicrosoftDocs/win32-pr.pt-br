---
description: Um determinado codificador dá suporte a determinadas categorias de parâmetro e, para cada uma dessas categorias, esse codificador permite certos valores.
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: Usando a enumeração EncoderValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755248150e81f963ea1c5c597ab04649c342944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967738"
---
# <a name="using-the-encodervalue-enumeration"></a><span data-ttu-id="e1c4a-103">Usando a enumeração EncoderValue</span><span class="sxs-lookup"><span data-stu-id="e1c4a-103">Using the EncoderValue Enumeration</span></span>

<span data-ttu-id="e1c4a-104">Um determinado codificador dá suporte a determinadas categorias de parâmetro e, para cada uma dessas categorias, esse codificador permite certos valores.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-104">A given encoder supports certain parameter categories, and for each of those categories, that encoder allows certain values.</span></span> <span data-ttu-id="e1c4a-105">Por exemplo, o codificador JPEG dá suporte à categoria de parâmetro EncoderValueQuality e os valores de parâmetro permitidos são os inteiros de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-105">For example, the JPEG encoder supports the EncoderValueQuality parameter category, and the allowable parameter values are the integers 0 through 100.</span></span> <span data-ttu-id="e1c4a-106">Alguns dos valores de parâmetro permitidos são os mesmos em vários codificadores.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-106">Some of the allowable parameter values are the same across several encoders.</span></span> <span data-ttu-id="e1c4a-107">Esses valores padrão são definidos na enumeração [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) em Gdiplusenums. h:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-107">These standard values are defined in the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration in Gdiplusenums.h:</span></span>


```
enum EncoderValue
{
   EncoderValueColorTypeCMYK,             // 0
   EncoderValueColorTypeYCCK,             // 1
   EncoderValueCompressionLZW,            // 2
   EncoderValueCompressionCCITT3,         // 3
   EncoderValueCompressionCCITT4,         // 4
   EncoderValueCompressionRle,            // 5
   EncoderValueCompressionNone,           // 6
   EncoderValueScanMethodInterlaced,      // 7
   EncoderValueScanMethodNonInterlaced,   // 8
   EncoderValueVersionGif87,              // 9
   EncoderValueVersionGif89,              // 10
   EncoderValueRenderProgressive,         // 11
   EncoderValueRenderNonProgressive,      // 12
   EncoderValueTransformRotate90,         // 13
   EncoderValueTransformRotate180,        // 14
   EncoderValueTransformRotate270,        // 15
   EncoderValueTransformFlipHorizontal,   // 16
   EncoderValueTransformFlipVertical,     // 17
   EncoderValueMultiFrame,                // 18
   EncoderValueLastFrame,                 // 19
   EncoderValueFlush,                     // 20
   EncoderValueFrameDimensionTime,        // 21
   EncoderValueFrameDimensionResolution,  // 22
   EncoderValueFrameDimensionPage         // 23
};
```



<span data-ttu-id="e1c4a-108">Uma das categorias de parâmetro com suporte pelo codificador JPEG é a categoria EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-108">One of the parameter categories supported by the JPEG encoder is the EncoderTransformation category.</span></span> <span data-ttu-id="e1c4a-109">Examinando a enumeração [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) , você pode especular (e você estaria correto) que a categoria EncoderTransformation permite os cinco valores a seguir:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-109">By examining the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration, you might speculate (and you would be correct) that the EncoderTransformation category allows the following five values:</span></span>


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



<span data-ttu-id="e1c4a-110">O aplicativo de console a seguir verifica se o codificador JPEG dá suporte à categoria de parâmetro EncoderTransformation e se há cinco valores permitidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-110">The following console application verifies that the JPEG encoder supports the EncoderTransformation parameter category and that there are five allowable values for such a parameter.</span></span> <span data-ttu-id="e1c4a-111">A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="e1c4a-111">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);
INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   // Create a Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);
   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);
   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);
   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);
   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);
   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);
   // Look at the first (index 0) EncoderParameter object in the array.
   printf("Parameter[0]\n");
   WCHAR strGuid[39];
   StringFromGUID2(pEncoderParameters->Parameter[0].Guid, strGuid, 39);
   wprintf(L"   The guid is %s.\n", strGuid);
   printf("   The data type is %d.\n", 
      pEncoderParameters->Parameter[0].Type);
   printf("   The number of values is %d.\n",
      pEncoderParameters->Parameter[0].NumberOfValues);
   free(pEncoderParameters);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="e1c4a-112">Ao executar o aplicativo de console anterior, você obtém uma saída semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-112">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



<span data-ttu-id="e1c4a-113">Você pode pesquisar o GUID em Gdiplusimaging. h e descobrir que a categoria desse objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-113">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderTransformation.</span></span> <span data-ttu-id="e1c4a-114">Em Gdiplusenums. h, a enumeração [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que o tipo de dados 4 é ValueLong (inteiro sem sinal de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="e1c4a-114">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 4 is ValueLong (32-bit unsigned integer).</span></span> <span data-ttu-id="e1c4a-115">O número de valores é cinco, então sabemos que o membro **Value** do objeto **EncoderParameter** é um ponteiro para uma matriz de cinco valores **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="e1c4a-115">The number of values is five, so we know that the **Value** member of the **EncoderParameter** object is a pointer to an array of five **ULONG** values.</span></span>

<span data-ttu-id="e1c4a-116">O código a seguir é uma continuação do aplicativo de console que é mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-116">The following code is a continuation of the console application that is shown in the preceding example.</span></span> <span data-ttu-id="e1c4a-117">O código lista os valores permitidos para um parâmetro EncoderTransformation:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-117">The code lists the allowable values for an EncoderTransformation parameter:</span></span>


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



<span data-ttu-id="e1c4a-118">O código anterior gerencia a saída a seguir:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-118">The preceding code produces the following output:</span></span>


```
The allowable values are  13  14  15  16  17
```



<span data-ttu-id="e1c4a-119">Os valores permitidos (13, 14, 15, 16 e 17) correspondem aos seguintes membros da enumeração [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="e1c4a-119">The allowable values (13, 14, 15, 16, and 17) correspond to the following members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
