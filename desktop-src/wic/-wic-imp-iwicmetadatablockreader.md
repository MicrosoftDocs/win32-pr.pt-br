---
description: Implementando o IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementando o IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828604"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="61f11-103">Implementando o IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="61f11-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="61f11-104">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="61f11-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="61f11-105">Vários blocos de metadados geralmente existem em uma imagem, cada um expondo diferentes tipos de informações em formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="61f11-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="61f11-106">No modelo do Windows Imaging Component (WIC), os manipuladores de metadados são componentes distintos que, como decodificadores, são detectáveis em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="61f11-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="61f11-107">Cada formato de metadados tem um manipulador separado, e cada um desses manipuladores de metadados pode ser usado com qualquer formato de imagem que ofereça suporte ao formato de metadados que ele manipula.</span><span class="sxs-lookup"><span data-stu-id="61f11-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="61f11-108">Portanto, se o formato de imagem oferecer suporte a EXIF, XMP, IPTC ou outro formato, você poderá aproveitar os manipuladores de metadados padrão para esses formatos fornecidos com o WIC e não precisará escrever o seu próprio.</span><span class="sxs-lookup"><span data-stu-id="61f11-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="61f11-109">É claro que, se você criar um novo formato de metadados, deverá gravar um manipulador de metadados para ele, que será descoberto e invocado em tempo de execução, assim como os padrões.</span><span class="sxs-lookup"><span data-stu-id="61f11-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="61f11-110">Se o formato de imagem for baseado em um formato TIFF ou JPEG, você não precisará escrever manipuladores de metadados (a menos que você desenvolva um formato de metadados novo ou proprietário).</span><span class="sxs-lookup"><span data-stu-id="61f11-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="61f11-111">Em contêineres TIFF e JPEG, blocos de metadados estão localizados em IFDs, e cada contêiner tem uma estrutura IFD diferente.</span><span class="sxs-lookup"><span data-stu-id="61f11-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="61f11-112">O WIC fornece manipuladores de IFD para ambos os formatos de contêiner que navegam na estrutura IFD e delegam aos manipuladores de metadados padrão para acessar os metadados dentro deles.</span><span class="sxs-lookup"><span data-stu-id="61f11-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="61f11-113">Portanto, se o formato da imagem for baseado em qualquer um desses contêineres, você poderá aproveitar automaticamente os manipuladores de IFD do WIC.</span><span class="sxs-lookup"><span data-stu-id="61f11-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="61f11-114">No entanto, se você tiver um formato de contêiner proprietário que tenha sua própria estrutura de metadados de nível superior exclusiva, deverá escrever um manipulador que possa navegar pela estrutura de nível superior e delegar para os manipuladores de metadados apropriados, assim como os manipuladores de IFD.)</span><span class="sxs-lookup"><span data-stu-id="61f11-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="61f11-115">Da mesma forma que o WIC fornece uma camada de abstração para aplicativos que permite trabalhar com todos os formatos de imagem da mesma maneira por meio de um conjunto consistente de interfaces, o WIC fornece uma camada de abstração para autores de codec em relação aos formatos de metadados.</span><span class="sxs-lookup"><span data-stu-id="61f11-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="61f11-116">Conforme observado anteriormente, os autores de codec geralmente não precisam trabalhar diretamente com os vários formatos de metadados que podem estar presentes em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="61f11-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="61f11-117">No entanto, cada autor de codec é responsável por fornecer uma maneira de enumerar os blocos de metadados para que um manipulador de metadados apropriado possa ser descoberto e instanciado para cada bloco.</span><span class="sxs-lookup"><span data-stu-id="61f11-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="61f11-118">Você deve implementar essa interface em sua classe de decodificação de nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="61f11-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="61f11-119">Talvez você também precise implementá-lo em sua classe de decodificador de nível de contêiner se seu formato de imagem expõe metadados globais fora de qualquer quadro de imagem individual.</span><span class="sxs-lookup"><span data-stu-id="61f11-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="61f11-120">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="61f11-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="61f11-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="61f11-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="61f11-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="61f11-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="61f11-123">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="61f11-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="61f11-124">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="61f11-124">GetContainerFormat</span></span>

<span data-ttu-id="61f11-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) é o mesmo que o método [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) na [implementação de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="61f11-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="61f11-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="61f11-126">GetCount</span></span>

<span data-ttu-id="61f11-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) retorna o número de blocos de metadados de nível superior associados ao quadro.</span><span class="sxs-lookup"><span data-stu-id="61f11-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="61f11-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="61f11-128">GetEnumerator</span></span>

<span data-ttu-id="61f11-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) retorna um enumerador que o chamador pode usar para enumerar os blocos de metadados no quadro e ler seus metadados.</span><span class="sxs-lookup"><span data-stu-id="61f11-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="61f11-130">Para implementar esse método, você precisa criar um leitor de metadados para cada bloco de metadados e implementar um objeto de enumeração que enumere sobre a coleção de leitores de metadados.</span><span class="sxs-lookup"><span data-stu-id="61f11-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="61f11-131">O objeto de enumeração deve implementar [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) para que você possa convertê-lo em IEnumUnknown ao retorná-lo no parâmetro *ppIEnumMetadata* .</span><span class="sxs-lookup"><span data-stu-id="61f11-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="61f11-132">Ao implementar o objeto de enumeração, você pode criar todos os leitores de metadados ao criar primeiro o objeto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) ou ao criar o objeto de enumeração pela primeira vez ou pode criá-los lentamente dentro da implementação do método [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) .</span><span class="sxs-lookup"><span data-stu-id="61f11-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="61f11-133">Em muitos casos, é mais eficiente criá-los lentamente, mas, no exemplo a seguir, os leitores de bloco são todos criados no construtor para economizar espaço.</span><span class="sxs-lookup"><span data-stu-id="61f11-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="61f11-134">Para criar os leitores de metadados, use o método [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) .</span><span class="sxs-lookup"><span data-stu-id="61f11-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="61f11-135">Ao invocar esse método, você passa o GUID do formato de contêiner no parâmetro *guidContainerFormat* .</span><span class="sxs-lookup"><span data-stu-id="61f11-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="61f11-136">Se você tiver uma preferência de fornecedor para um leitor de metadados, poderá passar o GUID do seu fornecedor preferido no parâmetro *pguidVendor* .</span><span class="sxs-lookup"><span data-stu-id="61f11-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="61f11-137">Por exemplo, se sua empresa escreve manipuladores de metadados e você deseja usar seu próprio, se estiver presente, você pode passar o GUID do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="61f11-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="61f11-138">Na maioria dos casos, basta passar **NULL** e deixar o sistema selecionar o leitor de metadados apropriado.</span><span class="sxs-lookup"><span data-stu-id="61f11-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="61f11-139">Se você solicitar um fornecedor específico e esse fornecedor tiver um leitor de metadados instalado no computador, o WIC retornará o leitor desse fornecedor.</span><span class="sxs-lookup"><span data-stu-id="61f11-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="61f11-140">No entanto, se o fornecedor solicitado não tiver um leitor de metadados instalado no computador e se houver um leitor de metadados apropriado disponível, esse leitor será retornado mesmo que não seja do fornecedor preferido.</span><span class="sxs-lookup"><span data-stu-id="61f11-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="61f11-141">Se não houver nenhum leitor de metadados no computador para o tipo de metadados no bloco, a fábrica de componentes retornará o manipulador de metadados desconhecido, que tratará o bloco de metadados como um BLOB (objeto binário grande) e desserializará o bloco de metadados do arquivo sem nenhuma tentativa de analisá-lo.</span><span class="sxs-lookup"><span data-stu-id="61f11-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="61f11-142">Para o parâmetro *dwOptions* , execute uma operação or entre o [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) apropriado com o [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)apropriado.</span><span class="sxs-lookup"><span data-stu-id="61f11-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="61f11-143">O **WICPersistOptions** descreve como seu contêiner é apresentado. Little-endian é o padrão.</span><span class="sxs-lookup"><span data-stu-id="61f11-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="61f11-144">O [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) especifica se você deseja recuperar o UnknownMetadataHandler se nenhum leitor de metadados for encontrado no computador que possa ler o formato de metadados de um bloco específico.</span><span class="sxs-lookup"><span data-stu-id="61f11-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="61f11-145">**WICMetadataCreationAllowUnknown** é o padrão e você sempre deve permitir a criação do UnknownMetadtataHandler.</span><span class="sxs-lookup"><span data-stu-id="61f11-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="61f11-146">O UnknownMetadataHandler trata os metadados não reconhecidos como um BLOB.</span><span class="sxs-lookup"><span data-stu-id="61f11-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="61f11-147">Ele não pode analisá-lo, mas o grava no fluxo como um BLOB e o mantém intacto quando é gravado no fluxo durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="61f11-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="61f11-148">Isso torna seguro criar manipuladores de metadados para metadados proprietários ou formatos de metadados que não são fornecidos com o sistema.</span><span class="sxs-lookup"><span data-stu-id="61f11-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="61f11-149">Como os metadados são preservados intactos, mesmo se nenhum manipulador estiver presente no computador que o reconhece, quando um manipulador de metadados apropriado for instalado posteriormente, os metadados ainda estarão lá e poderão ser lidos.</span><span class="sxs-lookup"><span data-stu-id="61f11-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="61f11-150">Se você não permitir a criação do UnknownMetadataHandler, a alternativa será descartar ou substituir os metadados não reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="61f11-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="61f11-151">Essa é uma forma de perda de dados.</span><span class="sxs-lookup"><span data-stu-id="61f11-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="61f11-152">Se você escrever seu próprio manipulador de metadados para metadados proprietários, nunca deverá incluir referências a nada fora do próprio bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="61f11-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="61f11-153">Embora o UnknownMetadataHandler preserve os metadados intactos, os metadados são movidos quando os arquivos são editados, e todas as referências a qualquer coisa fora de seu próprio bloco não serão mais válidas quando isso acontecer.</span><span class="sxs-lookup"><span data-stu-id="61f11-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="61f11-154">O parâmetro *pIStream* é o fluxo real que você está decodificando.</span><span class="sxs-lookup"><span data-stu-id="61f11-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="61f11-155">Antes de passar no fluxo, você deve procurar o início do bloco de metadados para o qual você está solicitando um leitor.</span><span class="sxs-lookup"><span data-stu-id="61f11-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="61f11-156">O leitor de metadados apropriado para o bloco de metadados na posição atual em [IStream](/windows/desktop/api/objidl/nn-objidl-istream) será retornado no parâmetro *ppiReader* .</span><span class="sxs-lookup"><span data-stu-id="61f11-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="61f11-157">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="61f11-157">GetReaderByIndex</span></span>

<span data-ttu-id="61f11-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) retorna o leitor de metadados no índice solicitado na coleção.</span><span class="sxs-lookup"><span data-stu-id="61f11-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61f11-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61f11-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="61f11-160">**Referência**</span><span class="sxs-lookup"><span data-stu-id="61f11-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="61f11-161">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="61f11-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="61f11-162">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="61f11-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="61f11-163">Implementando IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="61f11-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="61f11-164">Implementando IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="61f11-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="61f11-165">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="61f11-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="61f11-166">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="61f11-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
