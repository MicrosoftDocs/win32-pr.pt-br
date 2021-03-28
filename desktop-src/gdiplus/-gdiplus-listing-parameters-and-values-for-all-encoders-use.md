---
description: O aplicativo de console a seguir lista todos os parâmetros compatíveis com os vários codificadores instalados no computador.
ms.assetid: c80ad013-0b92-461f-8714-4b6d0cb6de0d
title: Listando parâmetros e valores para todos os codificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdaf522193f1074a28fe9f5ebb8a7afc2bade0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988752"
---
# <a name="listing-parameters-and-values-for-all-encoders"></a>Listando parâmetros e valores para todos os codificadores

O aplicativo de console a seguir lista todos os parâmetros compatíveis com os vários codificadores instalados no computador. A função Main chama [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) para descobrir quais codificadores estão disponíveis. Para cada codificador disponível, a função Main chama a função auxiliar ShowAllEncoderParameters.

A função ShowAllEncoderParameters chama o método [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) para descobrir quais parâmetros têm suporte em um determinado codificador. Para cada parâmetro com suporte, a função lista a categoria, o tipo de dados e o número de valores. A função ShowAllEncoderParameters se baseia em duas funções auxiliares: EncoderParameterCategoryFromGUID e ValueTypeFromULONG.


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

// Helper functions
void ShowAllEncoderParameters(ImageCodecInfo*);
HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars);
HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars);

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // Number of image encoders
   UINT  size;       // Size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfos, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);
    
   // For each ImageCodecInfo object in the array, show all parameters.
   for(UINT j = 0; j < num; ++j)
   { 
      ShowAllEncoderParameters(&(pImageCodecInfo[j]));
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}


/////////////////////////////////////////////////
// Helper functions

VOID ShowAllEncoderParameters(ImageCodecInfo* pImageCodecInfo)
{
   CONST MAX_CATEGORY_LENGTH = 50;
   CONST MAX_VALUE_TYPE_LENGTH = 50;
   WCHAR strParameterCategory[MAX_CATEGORY_LENGTH] = L"";
   WCHAR strValueType[MAX_VALUE_TYPE_LENGTH] = L"";

   wprintf(L"\n\n%s\n", pImageCodecInfo->MimeType);

   // Create a Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap bitmap(1, 1);

   // How big (in bytes) is the encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap.GetEncoderParameterListSize(&pImageCodecInfo->Clsid);
   printf("  The parameter list requires %d bytes.\n", listSize);

   if(listSize == 0)
      return;

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   if(pEncoderParameters == NULL)
      return;

   // Get the parameter list for the encoder.
   bitmap.GetEncoderParameterList(
      &pImageCodecInfo->Clsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("  There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   // For each EncoderParameter object in the array, list the
   // parameter category, data type, and number of values.
   for(UINT k = 0; k < pEncoderParameters->Count; ++k)
   {
      EncoderParameterCategoryFromGUID(
         pEncoderParameters->Parameter[k].Guid, strParameterCategory, MAX_CATEGORY_LENGTH);

      ValueTypeFromULONG(
         pEncoderParameters->Parameter[k].Type, strValueType, MAX_VALUE_TYPE_LENGTH);

      printf("    Parameter[%d]\n", k);
      wprintf(L"      The category is %s.\n", strParameterCategory);
      wprintf(L"      The data type is %s.\n", strValueType);

      printf("      The number of values is %d.\n",
      pEncoderParameters->Parameter[k].NumberOfValues); 
   } // for

   free(pEncoderParameters);
} // ShowAllEncoderParameters


HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   if(guid == EncoderCompression)
      hr = StringCchCopyW(category, maxChars, L"Compression");
   else if(guid == EncoderColorDepth)
      hr = StringCchCopyW(category, maxChars, L"ColorDepth");
   else if(guid == EncoderScanMethod)
      hr = StringCchCopyW(category, maxChars, L"ScanMethod");
   else if(guid == EncoderVersion)
      hr = StringCchCopyW(category, maxChars, L"Version");
   else if(guid == EncoderRenderMethod)
      hr = StringCchCopyW(category, maxChars, L"RenderMethod");
   else if(guid == EncoderQuality)
      hr = StringCchCopyW(category, maxChars, L"Quality");
   else if(guid == EncoderTransformation)
      hr = StringCchCopyW(category, maxChars, L"Transformation");
   else if(guid == EncoderLuminanceTable)
      hr = StringCchCopyW(category, maxChars, L"LuminanceTable");
   else if(guid == EncoderChrominanceTable)
      hr = StringCchCopyW(category, maxChars, L"ChrominanceTable");
   else if(guid == EncoderSaveFlag)
      hr = StringCchCopyW(category, maxChars, L"SaveFlag");
   else
      hr = StringCchCopyW(category, maxChars, L"Unknown category");

   return hr;
} // EncoderParameterCategoryFromGUID


HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* valueTypes[] = {
      L"Nothing",                  // 0
      L"ValueTypeByte",            // 1
      L"ValueTypeASCII",           // 2
      L"ValueTypeShort",           // 3
      L"ValueTypeLong",            // 4
      L"ValueTypeRational",        // 5
      L"ValueTypeLongRange",       // 6
      L"ValueTypeUndefined",       // 7
      L"ValueTypeRationalRange"};  // 8

   hr = StringCchCopyW(strValueType, maxChars, valueTypes[index]);
   return hr;

} // ValueTypeFromULONG
```



Ao executar o aplicativo de console anterior, você obtém uma saída semelhante à seguinte:


```
image/bmp
  The parameter list requires 0 bytes.

image/jpeg
  The parameter list requires 172 bytes.
  There are 4 EncoderParameter objects in the array.
    Parameter[0]
      The category is Transformation.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is Quality.
      The data type is LongRange.
      The number of values is 1.
    Parameter[2]
      The category is LuminanceTable.
      The data type is Short.
      The number of values is 0.
    Parameter[3]
      The category is ChrominanceTable.
      The data type is Short.
      The number of values is 0.

image/gif
  The parameter list requires 0 bytes.

image/tiff
  The parameter list requires 160 bytes.
  There are 3 EncoderParameter objects in the array.
    Parameter[0]
      The category is Compression.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is ColorDepth.
      The data type is Long.
      The number of values is 5.
    Parameter[2]
      The category is SaveFlag.
      The data type is Long.
      The number of values is 1.

image/png
  The parameter list requires 0 bytes.
```



Você pode desenhar as seguintes conclusões examinando a saída do programa anterior:

-   O codificador JPEG dá suporte às categorias de parâmetro Transformation, Quality, Luminescênciatable e ChrominanceTable.
-   O codificador TIFF dá suporte às categorias de parâmetro Compression, ColorDepth e SaveFlag.

Você também pode ver o número de valores aceitáveis para cada categoria de parâmetro. Por exemplo, você pode ver que a categoria de parâmetro ColorDepth (codec TIFF) tem cinco valores do tipo **ULONG**. O código a seguir lista esses cinco valores. Suponha que **pEncoderParameters** é um ponteiro para um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que representa o codificador TIFF.


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[1].Value);
ULONG numVals = pEncoderParameters->Parameter[1].NumberOfValues;
printf("\nThe allowable values for ColorDepth are\n");

for(ULONG k = 0; k < numVals; ++k)
{
   printf("  %u\n", pUlong[k]);
}
            
```



O código anterior gerencia a saída a seguir:


```
The allowable values for ColorDepth are
  1
  4
  8
  24
  32
            
```



> [!Note]  
> Em alguns casos, os valores em um objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) são os valores numéricos dos elementos da enumeração [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . No entanto, os números na lista anterior não se relacionam com a enumeração **EncoderValue** . Os números significam 1 bit por pixel, 2 bits por pixel e assim por diante.

 

Se você escrever um código semelhante ao exemplo anterior para investigar os valores permitidos para as outras categorias de parâmetro, obterá um resultado semelhante ao seguinte.



| Parâmetro de codificador JPEG | Valores permitidos                                                                                                                                                                                                 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transformação         | EncoderValueTransformRotate90 EncoderValueTransformRotate180<br/>  EncoderValueTransformRotate270<br/>  EncoderValueTransformFlipHorizontal<br/>  EncoderValueTransformFlipVertical<br/> |
| Qualidade                | 0 a 100                                                                                                                                                                                                    |



 



| Parâmetro de codificador TIFF | Valores permitidos                                                                                                                                                                             |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compactação            | EncoderValueCompressionLZW EncoderValueCompressionCCITT3<br/>  EncoderValueCompressionCCITT4<br/>  EncoderValueCompressionRle<br/>  EncoderValueCompressionNone<br/> |
| ColorDepth             | 1, 4, 8, 24, 32                                                                                                                                                                              |
| SaveFlag               | EncoderValueMultiFrame                                                                                                                                                                       |



 

> [!Note]  
> Se a largura e a altura de uma imagem JPEG forem múltiplos de 16, você poderá aplicar qualquer uma das transformações permitidas pela categoria de parâmetro EncoderTransformation (por exemplo, rotação de 90 graus) sem perda de informações.

 

 

 
