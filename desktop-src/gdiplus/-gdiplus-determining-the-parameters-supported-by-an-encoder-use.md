---
description: 'A classe Image fornece o método Image:: GetEncoderParameterList para que você possa determinar os parâmetros com suporte em um determinado codificador de imagem.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Determinando os parâmetros com suporte de um codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988883"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="2e77d-103">Determinando os parâmetros com suporte de um codificador</span><span class="sxs-lookup"><span data-stu-id="2e77d-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="2e77d-104">A classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornece o método [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) para que você possa determinar os parâmetros com suporte em um determinado codificador de imagem.</span><span class="sxs-lookup"><span data-stu-id="2e77d-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="2e77d-105">O método **Image:: GetEncoderParameterList** retorna uma matriz de objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="2e77d-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="2e77d-106">Você deve alocar um buffer para receber essa matriz antes de chamar **Image:: GetEncoderParameterList**.</span><span class="sxs-lookup"><span data-stu-id="2e77d-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="2e77d-107">Você pode chamar [**Image:: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) para determinar o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="2e77d-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="2e77d-108">O aplicativo de console a seguir obtém a lista de parâmetros para o codificador JPEG.</span><span class="sxs-lookup"><span data-stu-id="2e77d-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="2e77d-109">A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="2e77d-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   // Create Bitmap (inherited from Image) object so that we can call
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

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="2e77d-110">Ao executar o aplicativo de console anterior, você obtém uma saída semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="2e77d-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="2e77d-111">Cada um dos objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) na matriz tem os quatro membros de dados públicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="2e77d-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="2e77d-112">O código a seguir é uma continuação do aplicativo de console mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2e77d-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="2e77d-113">O código examina o segundo objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) na matriz retornada pela [**imagem:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span><span class="sxs-lookup"><span data-stu-id="2e77d-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="2e77d-114">O código chama [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), que é uma função de sistema declarada em Objbase. h, para converter o membro **GUID** do objeto **EncoderParameter** em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e77d-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



<span data-ttu-id="2e77d-115">O código anterior gerencia a saída a seguir:</span><span class="sxs-lookup"><span data-stu-id="2e77d-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="2e77d-116">Você pode pesquisar o GUID em Gdiplusimaging. h e descobrir que a categoria desse objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é EncoderQuality.</span><span class="sxs-lookup"><span data-stu-id="2e77d-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="2e77d-117">Você pode usar essa categoria (EncoderQuality) do parâmetro para definir o nível de compactação de uma imagem JPEG.</span><span class="sxs-lookup"><span data-stu-id="2e77d-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="2e77d-118">Em Gdiplusenums. h, a enumeração [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que o tipo de dados 6 é **ValueLongRange**.</span><span class="sxs-lookup"><span data-stu-id="2e77d-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="2e77d-119">Um intervalo longo é um par de valores **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="2e77d-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="2e77d-120">O número de valores é um, então sabemos que o membro **Value** do objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é um ponteiro para uma matriz que tem um elemento.</span><span class="sxs-lookup"><span data-stu-id="2e77d-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="2e77d-121">Esse elemento é um par de valores **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="2e77d-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="2e77d-122">O código a seguir é uma continuação do aplicativo de console que é mostrado nos dois exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="2e77d-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="2e77d-123">O código define um tipo de dados chamado **PLONGRANGE** (ponteiro para um intervalo longo).</span><span class="sxs-lookup"><span data-stu-id="2e77d-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="2e77d-124">Uma variável do tipo **PLONGRANGE** é usada para extrair os valores mínimo e máximo que podem ser passados como uma configuração de qualidade para o codificador JPEG.</span><span class="sxs-lookup"><span data-stu-id="2e77d-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



<span data-ttu-id="2e77d-125">O código anterior gerencia a saída a seguir:</span><span class="sxs-lookup"><span data-stu-id="2e77d-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="2e77d-126">No exemplo anterior, o valor retornado no objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é um par de valores **ULONG** que indicam os valores mínimo e máximo possíveis para o parâmetro de qualidade.</span><span class="sxs-lookup"><span data-stu-id="2e77d-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="2e77d-127">Em alguns casos, os valores retornados em um objeto **EncoderParameter** são membros da enumeração [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) .</span><span class="sxs-lookup"><span data-stu-id="2e77d-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="2e77d-128">Os tópicos a seguir abordam a enumeração **EncoderValue** e os métodos para listar possíveis valores de parâmetro com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="2e77d-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="2e77d-129">Usando a enumeração EncoderValue</span><span class="sxs-lookup"><span data-stu-id="2e77d-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="2e77d-130">Listando parâmetros e valores para todos os codificadores</span><span class="sxs-lookup"><span data-stu-id="2e77d-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
