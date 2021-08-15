---
description: 'A classe Image fornece o método Image:: GetEncoderParameterList para que você possa determinar os parâmetros com suporte em um determinado codificador de imagem.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Determinando os parâmetros com suporte de um codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c842b14a2d14af578eede428e79018a2d266ea6133ed61a9bd0736e8dadc97e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977566"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Determinando os parâmetros com suporte de um codificador

A classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornece o método [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) para que você possa determinar os parâmetros com suporte em um determinado codificador de imagem. O método **Image:: GetEncoderParameterList** retorna uma matriz de objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Você deve alocar um buffer para receber essa matriz antes de chamar **Image:: GetEncoderParameterList**. Você pode chamar [**Image:: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) para determinar o tamanho do buffer necessário.

O aplicativo de console a seguir obtém a lista de parâmetros para o codificador JPEG. A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



Ao executar o aplicativo de console anterior, você obtém uma saída semelhante à seguinte:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Cada um dos objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) na matriz tem os quatro membros de dados públicos a seguir:

O código a seguir é uma continuação do aplicativo de console mostrado no exemplo anterior. O código examina o segundo objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) na matriz retornada pela [**imagem:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist). O código chama [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), que é uma função de sistema declarada em Objbase. h, para converter o membro **GUID** do objeto **EncoderParameter** em uma cadeia de caracteres.


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



O código anterior gerencia a saída a seguir:


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



Você pode pesquisar o GUID em Gdiplusimaging. h e descobrir que a categoria desse objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é EncoderQuality. Você pode usar essa categoria (EncoderQuality) do parâmetro para definir o nível de compactação de uma imagem JPEG.

Em Gdiplusenums. h, a enumeração [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que o tipo de dados 6 é **ValueLongRange**. Um intervalo longo é um par de valores **ULONG** .

O número de valores é um, então sabemos que o membro **Value** do objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é um ponteiro para uma matriz que tem um elemento. Esse elemento é um par de valores **ULONG** .

O código a seguir é uma continuação do aplicativo de console que é mostrado nos dois exemplos anteriores. O código define um tipo de dados chamado **PLONGRANGE** (ponteiro para um intervalo longo). Uma variável do tipo **PLONGRANGE** é usada para extrair os valores mínimo e máximo que podem ser passados como uma configuração de qualidade para o codificador JPEG.


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



O código anterior gerencia a saída a seguir:


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



No exemplo anterior, o valor retornado no objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) é um par de valores **ULONG** que indicam os valores mínimo e máximo possíveis para o parâmetro de qualidade. Em alguns casos, os valores retornados em um objeto **EncoderParameter** são membros da enumeração [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . Os tópicos a seguir abordam a enumeração **EncoderValue** e os métodos para listar possíveis valores de parâmetro com mais detalhes:

-   [Usando a enumeração EncoderValue](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Listando parâmetros e valores para todos os codificadores](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
