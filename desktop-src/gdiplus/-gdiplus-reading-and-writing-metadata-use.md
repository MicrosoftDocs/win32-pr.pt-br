---
description: Alguns arquivos de imagem contêm metadados que você pode ler para determinar os recursos da imagem.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lendo e gravando metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f599c1134efc8768d0b6ed59deaae8adf9f6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647103"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="df274-103">Lendo e gravando metadados</span><span class="sxs-lookup"><span data-stu-id="df274-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="df274-104">Alguns arquivos de imagem contêm metadados que você pode ler para determinar os recursos da imagem.</span><span class="sxs-lookup"><span data-stu-id="df274-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="df274-105">Por exemplo, uma fotografia digital pode conter metadados que você pode ler para determinar a marca e modelo da câmera usada para capturar a imagem.</span><span class="sxs-lookup"><span data-stu-id="df274-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="df274-106">Com o Windows GDI+, você pode ler os metadados existentes e também pode gravar novos metadados em arquivos de imagem.</span><span class="sxs-lookup"><span data-stu-id="df274-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="df274-107">O GDI+ fornece uma maneira uniforme de armazenar e recuperar metadados de arquivos de imagem em vários formatos.</span><span class="sxs-lookup"><span data-stu-id="df274-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="df274-108">No GDI+, um pedaço de metadados é chamado de *item de propriedade*.</span><span class="sxs-lookup"><span data-stu-id="df274-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="df274-109">Você pode armazenar e recuperar metadados chamando os métodos **SetPropertyItem** e **GetPropertyItem** da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , e não precisa se preocupar com os detalhes de como um formato de arquivo específico armazena esses metadados.</span><span class="sxs-lookup"><span data-stu-id="df274-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="df274-110">Atualmente, o GDI+ dá suporte a metadados para os formatos de arquivo TIFF, JPEG, EXIF e PNG.</span><span class="sxs-lookup"><span data-stu-id="df274-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="df274-111">O formato Exif, que especifica como armazenar imagens capturadas por câmeras digitais ainda, é criado com base nos formatos TIFF e JPEG.</span><span class="sxs-lookup"><span data-stu-id="df274-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="df274-112">O EXIF usa o formato TIFF para dados de pixel não compactados e o formato JPEG para dados de pixel compactados.</span><span class="sxs-lookup"><span data-stu-id="df274-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="df274-113">O GDI+ define um conjunto de marcas de propriedade que identificam itens de propriedade.</span><span class="sxs-lookup"><span data-stu-id="df274-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="df274-114">Determinadas marcas são de finalidade geral; ou seja, eles têm suporte de todos os formatos de arquivo mencionados no parágrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="df274-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="df274-115">Outras marcas são de finalidade especial e se aplicam apenas a determinados formatos.</span><span class="sxs-lookup"><span data-stu-id="df274-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="df274-116">Se você tentar salvar um item de propriedade em um arquivo que não dá suporte a esse item de propriedade, o GDI+ ignorará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="df274-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="df274-117">Mais especificamente, o método [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) retorna PropertyNotSupported.</span><span class="sxs-lookup"><span data-stu-id="df274-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="df274-118">Você pode determinar os itens de propriedade que são armazenados em um arquivo de imagem chamando [**Image:: GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span><span class="sxs-lookup"><span data-stu-id="df274-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="df274-119">Se você tentar recuperar um item de propriedade que não está no arquivo, o GDI+ ignorará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="df274-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="df274-120">Mais especificamente, o método [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) retorna PropertyNotFound.</span><span class="sxs-lookup"><span data-stu-id="df274-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="df274-121">Lendo metadados de um arquivo</span><span class="sxs-lookup"><span data-stu-id="df274-121">Reading Metadata from a File</span></span>

<span data-ttu-id="df274-122">O aplicativo de console a seguir chama o método **GetPropertySize** de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para determinar quantas partes de metadados estão no arquivo FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="df274-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


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



<span data-ttu-id="df274-123">O código anterior, junto com um arquivo específico, FakePhoto.jpg, produziu a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="df274-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="df274-124">O GDI+ armazena uma parte individual dos metadados em um objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .</span><span class="sxs-lookup"><span data-stu-id="df274-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="df274-125">Você pode chamar o método **GetAllPropertyItems** da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para recuperar todos os metadados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="df274-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="df274-126">O método **GetAllPropertyItems** retorna uma matriz de objetos **PropertyItem** .</span><span class="sxs-lookup"><span data-stu-id="df274-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="df274-127">Antes de chamar **GetAllPropertyItems**, você deve alocar um buffer grande o suficiente para receber essa matriz.</span><span class="sxs-lookup"><span data-stu-id="df274-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="df274-128">Você pode chamar o método **GetPropertySize** da classe **Image** para obter o tamanho (em bytes) do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="df274-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="df274-129">Um objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) tem os quatro membros públicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="df274-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            |                                                                                                                                                                                                                                                                                                        |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df274-130">**id**</span><span class="sxs-lookup"><span data-stu-id="df274-130">**id**</span></span>     | <span data-ttu-id="df274-131">Uma marca que identifica o item de metadados.</span><span class="sxs-lookup"><span data-stu-id="df274-131">A tag that identifies the metadata item.</span></span> <span data-ttu-id="df274-132">Os valores que podem ser atribuídos à **ID** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime e like) são definidos em Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="df274-132">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="df274-133">**length**</span><span class="sxs-lookup"><span data-stu-id="df274-133">**length**</span></span> | <span data-ttu-id="df274-134">O comprimento, em bytes, da matriz de valores apontada pelo membro de dados de **valor** .</span><span class="sxs-lookup"><span data-stu-id="df274-134">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="df274-135">Observe que, se o membro de dados de **tipo** for definido como PropertyTagTypeASCII, o membro de dados de comprimento será o **comprimento** de uma cadeia de caracteres terminada em nulo, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="df274-135">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="df274-136">**tipo**</span><span class="sxs-lookup"><span data-stu-id="df274-136">**type**</span></span>   | <span data-ttu-id="df274-137">O tipo de dados dos valores na matriz apontados pelo membro de dados de valor.</span><span class="sxs-lookup"><span data-stu-id="df274-137">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="df274-138">As constantes (PropertyTagTypeByte, PropertyTagTypeASCII e like) que representam vários tipos de dados são descritas em [**constantes de tipo de marca de propriedade de imagem**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="df274-138">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="df274-139">**value**</span><span class="sxs-lookup"><span data-stu-id="df274-139">**value**</span></span>  | <span data-ttu-id="df274-140">Um ponteiro para uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="df274-140">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="df274-141">O aplicativo de console a seguir lê e exibe as sete partes dos metadados no arquivo FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="df274-141">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="df274-142">A função main depende da função auxiliar PropertyTypeFromWORD, que é mostrada após a função main.</span><span class="sxs-lookup"><span data-stu-id="df274-142">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


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



<span data-ttu-id="df274-143">O aplicativo de console anterior produz a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="df274-143">The preceding console application produces the following output:</span></span>


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



<span data-ttu-id="df274-144">A saída anterior mostra um número de ID hexadecimal para cada item de propriedade.</span><span class="sxs-lookup"><span data-stu-id="df274-144">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="df274-145">Você pode pesquisar esses números de ID nas [constantes da marca de propriedade da imagem](-gdiplus-constant-image-property-tag-constants.md) e descobrir que elas representam as seguintes marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="df274-145">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="df274-146">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="df274-146">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="df274-147">Marca de propriedade</span><span class="sxs-lookup"><span data-stu-id="df274-147">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df274-148">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="df274-148">0x0320 0x010f</span></span><br/>  <span data-ttu-id="df274-149">0x0110</span><span class="sxs-lookup"><span data-stu-id="df274-149">0x0110</span></span><br/>  <span data-ttu-id="df274-150">0x9003</span><span class="sxs-lookup"><span data-stu-id="df274-150">0x9003</span></span><br/>  <span data-ttu-id="df274-151">0x829a</span><span class="sxs-lookup"><span data-stu-id="df274-151">0x829a</span></span><br/>  <span data-ttu-id="df274-152">0x5090</span><span class="sxs-lookup"><span data-stu-id="df274-152">0x5090</span></span><br/>  <span data-ttu-id="df274-153">0x5091</span><span class="sxs-lookup"><span data-stu-id="df274-153">0x5091</span></span><br/> | <span data-ttu-id="df274-154">PropertyTagImageTitle PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="df274-154">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="df274-155">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="df274-155">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="df274-156">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="df274-156">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="df274-157">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="df274-157">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="df274-158">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="df274-158">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="df274-159">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="df274-159">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="df274-160">O segundo item de propriedade (índice 1) na lista tem a **ID** PropertyTagEquipMake e o **tipo** PropertyTagTypeASCII.</span><span class="sxs-lookup"><span data-stu-id="df274-160">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="df274-161">O exemplo a seguir, que é uma continuação do aplicativo de console anterior, exibe o valor desse item de propriedade:</span><span class="sxs-lookup"><span data-stu-id="df274-161">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="df274-162">A linha de código anterior produz a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="df274-162">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="df274-163">O quinto (índice 4) do item de propriedade na lista tem a **ID** PropertyTagExifExposureTime e o **tipo** PropertyTagTypeRational.</span><span class="sxs-lookup"><span data-stu-id="df274-163">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="df274-164">Esse tipo de dados (PropertyTagTypeRational) é um par de s **longos**.</span><span class="sxs-lookup"><span data-stu-id="df274-164">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="df274-165">O exemplo a seguir, que é uma continuação do aplicativo de console anterior, exibe esses dois valores **longos** como uma fração.</span><span class="sxs-lookup"><span data-stu-id="df274-165">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="df274-166">Essa fração, 1/125, é o tempo de exposição medido em segundos.</span><span class="sxs-lookup"><span data-stu-id="df274-166">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="df274-167">O código anterior gerencia a saída a seguir:</span><span class="sxs-lookup"><span data-stu-id="df274-167">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="df274-168">Gravando metadados em um arquivo</span><span class="sxs-lookup"><span data-stu-id="df274-168">Writing Metadata to a File</span></span>

<span data-ttu-id="df274-169">Para gravar um item de metadados em um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , inicialize um objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) e, em seguida, passe o endereço desse objeto **PropertyItem** para o método **SetPropertyItem** do objeto **Image** .</span><span class="sxs-lookup"><span data-stu-id="df274-169">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="df274-170">O aplicativo de console a seguir grava um item (o título da imagem) de metadados em um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e, em seguida, salva a imagem no arquivo de disco FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="df274-170">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="df274-171">A função main depende da função auxiliar GetEncoderClsid, que é mostrada no tópico [recuperando o identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="df274-171">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
