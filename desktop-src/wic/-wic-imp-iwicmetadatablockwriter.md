---
description: Implementando IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementando IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506266"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="e6e50-103">Implementando IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="e6e50-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="e6e50-104">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="e6e50-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="e6e50-105">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="e6e50-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="e6e50-106">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="e6e50-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="e6e50-107">AddWriter</span><span class="sxs-lookup"><span data-stu-id="e6e50-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="e6e50-108">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="e6e50-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="e6e50-109">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="e6e50-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="e6e50-110">A classe de codificação no nível do quadro implementa essa interface para expor todos os blocos de metadados e solicitar o gravador de metadados apropriado para cada bloco.</span><span class="sxs-lookup"><span data-stu-id="e6e50-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="e6e50-111">Se o formato de imagem der suporte a metadados globais, fora de qualquer quadro individual, você também deverá implementar essa interface na classe de codificador de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="e6e50-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="e6e50-112">Para obter uma discussão mais detalhada sobre manipuladores de metadados, consulte a seção sobre o [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) na seção sobre como implementar um decodificador de WIC-Enabled.</span><span class="sxs-lookup"><span data-stu-id="e6e50-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="e6e50-113">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="e6e50-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="e6e50-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa um [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) para inicializar o gravador de bloco.</span><span class="sxs-lookup"><span data-stu-id="e6e50-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="e6e50-115">Você pode obter o **IWICMetadataBlockReader** do decodificador que decodificava a imagem.</span><span class="sxs-lookup"><span data-stu-id="e6e50-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="e6e50-116">Como inicializar o [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) com um [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instancia um gravador de metadados para cada leitor de metadados exposto pelo objeto **IWICMetadataBlockReader** , o aplicativo não precisa solicitar explicitamente um gravador para cada bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="e6e50-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="e6e50-117">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="e6e50-117">GetWriterByIndex</span></span>

<span data-ttu-id="e6e50-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) retorna o objeto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) para o enésimo bloco de metadados, em que n é o valor passado no parâmetro *nIndex* .</span><span class="sxs-lookup"><span data-stu-id="e6e50-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="e6e50-119">Se não houver nenhum gravador de metadados registrado que possa manipular o tipo de metadados no enésimo bloco, a fábrica de componentes retornará o manipulador de metadados desconhecido, que tratará o bloco de metadados como um BLOB (objeto binário grande).</span><span class="sxs-lookup"><span data-stu-id="e6e50-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="e6e50-120">Ele o serializará como um fluxo de bits sem tentar analisá-lo.</span><span class="sxs-lookup"><span data-stu-id="e6e50-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="e6e50-121">AddWriter</span><span class="sxs-lookup"><span data-stu-id="e6e50-121">AddWriter</span></span>

<span data-ttu-id="e6e50-122">O [**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permite que um chamador adicione um novo gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="e6e50-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="e6e50-123">Isso será necessário se um aplicativo quiser adicionar metadados de um formato diferente dos blocos de metadados existentes.</span><span class="sxs-lookup"><span data-stu-id="e6e50-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="e6e50-124">Por exemplo, um aplicativo pode querer adicionar alguns metadados XMP.</span><span class="sxs-lookup"><span data-stu-id="e6e50-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="e6e50-125">Se não houver nenhum bloco de metadados XMP existente, o aplicativo deverá criar uma instância de um gravador de metadados XMP e usar o método **AddWriter** para incluí-lo na coleção de gravadores de metadados.</span><span class="sxs-lookup"><span data-stu-id="e6e50-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="e6e50-126">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="e6e50-126">SetWriterByIndex</span></span>

<span data-ttu-id="e6e50-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) é usado para adicionar um gravador de metadados em um índice específico na coleção.</span><span class="sxs-lookup"><span data-stu-id="e6e50-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="e6e50-128">Se um gravador de metadados existir no momento nesse índice, o novo deverá substituí-lo.</span><span class="sxs-lookup"><span data-stu-id="e6e50-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="e6e50-129">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="e6e50-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="e6e50-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) é usado para remover um gravador de metadados da coleção.</span><span class="sxs-lookup"><span data-stu-id="e6e50-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6e50-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6e50-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e6e50-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e6e50-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6e50-133">Implementando IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="e6e50-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="e6e50-134">Instalação e registro de CODEC</span><span class="sxs-lookup"><span data-stu-id="e6e50-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="e6e50-135">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e6e50-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="e6e50-136">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="e6e50-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



