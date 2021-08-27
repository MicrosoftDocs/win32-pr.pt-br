---
description: Alguns arquivos de imagem contêm metadados que você pode ler para determinar os recursos da imagem.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lendo e escrevendo metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b965285e2d8a4666ef86b78cdc5dbb9ed38c55ee7c84b4a93f1dbe80141efa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114926"
---
# <a name="reading-and-writing-metadata"></a>Lendo e escrevendo metadados

Alguns arquivos de imagem contêm metadados que você pode ler para determinar os recursos da imagem. Por exemplo, uma fotografia digital pode conter metadados que você pode ler para determinar a marca e modelo da câmera usada para capturar a imagem. Com Windows GDI+, você pode ler metadados existentes e também gravar novos metadados em arquivos de imagem.

GDI+ fornece uma maneira uniforme de armazenar e recuperar metadados de arquivos de imagem em vários formatos. No GDI+, uma parte dos metadados é chamada de item *de propriedade*. Você pode armazenar e recuperar metadados chamando os métodos **SetPropertyItem** e **GetPropertyItem** da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e não precisa se preocupar com os detalhes de como um formato de arquivo específico armazena esses metadados.

GDI+ atualmente dá suporte a metadados para os formatos de arquivo TIFF, JPEG, Exif e PNG. O formato Exif, que especifica como armazenar imagens capturadas por câmeras ainda digitais, é criado com base nos formatos TIFF e JPEG. Exif usa o formato TIFF para dados de pixel descompactados e o formato JPEG para dados de pixel compactados.

GDI+ define um conjunto de marcas de propriedade que identificam itens de propriedade. Determinadas marcas são de uso geral; ou seja, eles têm suporte em todos os formatos de arquivo mencionados no parágrafo anterior. Outras marcas são de finalidade especial e se aplicam somente a determinados formatos. Se você tentar salvar um item de propriedade em um arquivo que não dá suporte a esse item de propriedade, GDI+ ignorará a solicitação. Mais especificamente, o [**método Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) retorna PropertyNotSupported.

Você pode determinar os itens de propriedade armazenados em um arquivo de imagem chamando [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist). Se você tentar recuperar um item de propriedade que não está no arquivo, GDI+ ignorará a solicitação. Mais especificamente, o [**método Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) retorna PropertyNotFound.

## <a name="reading-metadata-from-a-file"></a>Lendo metadados de um arquivo

O aplicativo de console a seguir chama o **método GetPropertySize** de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para determinar quantas partes de metadados estão no arquivo FakePhoto.jpg.


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



O código anterior, juntamente com um arquivo específico, FakePhoto.jpg, produziu a seguinte saída:


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI+ armazena uma parte individual dos metadados em um [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) Você pode chamar o **método GetAllPropertyItems** da [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para recuperar todos os metadados de um arquivo. O **método GetAllPropertyItems** retorna uma matriz de **objetos PropertyItem.** Antes de chamar **GetAllPropertyItems**, você deve alocar um buffer grande o suficiente para receber essa matriz. Você pode chamar o **método GetPropertySize** da classe **Image** para obter o tamanho (em bytes) do buffer necessário.

Um [**objeto PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) tem os quatro membros públicos a seguir:



|            | Descrição                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | Uma marca que identifica o item de metadados. Os valores que podem ser atribuídos à **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime e outros) são definidos em Gdiplusimaging.h.                                                                                           |
| **length** | O comprimento, em bytes, da matriz de valores apontados pelo membro **de dados** de valor. Observe que,  se o membro de dados de tipo estiver definido como  PropertyTagTypeASCII, o membro de dados de comprimento será o comprimento de uma cadeia de caracteres terminada em nulo, incluindo o terminador NULL.                        |
| **tipo**   | O tipo de dados dos valores na matriz apontado pelo membro de dados de valor. Constantes (PropertyTagTypeByte, PropertyTagTypeASCII e assim por diante) que representam vários tipos de dados são descritas em [**Constantes**](-gdiplus-constant-image-property-tag-type-constants.md)de tipo de marca de propriedade de imagem . |
| **value**  | Um ponteiro para uma matriz de valores.                                                                                                                                                                                                                                                                       |



 

O aplicativo de console a seguir lê e exibe as sete partes de metadados no arquivo FakePhoto.jpg. A função principal se baseia na função auxiliar PropertyTypeFromWORD, que é mostrada após a função principal.


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



O aplicativo de console anterior produz a seguinte saída:


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



A saída anterior mostra um número de ID hexadecimal para cada item de propriedade. Você pode procurar esses números de ID em [Constantes](-gdiplus-constant-image-property-tag-constants.md) de Marca de Propriedade de Imagem e descobrir que eles representam as marcas de propriedade a seguir.



| Valor hexadecimal                                                                                                       | Marca de propriedade                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010f<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | PropertyTagImageTitle PropertyTagEquipMake<br/>  PropertyTagEquipModel<br/>  PropertyTagExifDTOriginal<br/>  PropertyTagExifExposureTime<br/>  PropertyTagLuminanceTable<br/>  PropertyTagChrominanceTable<br/> |



 

O segundo item de propriedade (índice 1) na lista tem **a id** PropertyTagEquipMake e **o tipo** PropertyTagTypeASCII. O exemplo a seguir, que é uma continuação do aplicativo de console anterior, exibe o valor desse item de propriedade:


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



A linha de código anterior produz a seguinte saída:


```
The equipment make is Northwind Traders.
```



O quinto item de propriedade (índice 4) na lista tem **a id** PropertyTagExifExposureTime e **o tipo** PropertyTagTypeRational. Esse tipo de dados (PropertyTagTypeRational) é um par **de LONG** s. O exemplo a seguir, que é uma continuação do aplicativo de console anterior, exibe esses dois **valores LONG** como uma fração. Essa fração, 1/125, é o tempo de exposição medido em segundos.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



O código anterior gerencia a saída a seguir:


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Escrevendo metadados em um arquivo

Para gravar um item de metadados em um objeto [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) inicialize um objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) e, em seguida, passe o endereço desse objeto **PropertyItem** para o **método SetPropertyItem** do objeto **Image.**

O aplicativo de console a seguir grava um item (o título da imagem) de metadados em um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e salva a imagem no arquivo de disco FakePhoto2.jpg. A função principal se baseia na função auxiliar GetEncoderClsid, que é mostrada no tópico Recuperando o Identificador de Classe para um [Codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
