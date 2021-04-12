---
title: Suporte ao código de tempo SMPTE
description: Suporte ao código de tempo SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- SDK do Windows Media Format, códigos de tempo SMPTE
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- SDK do Windows Media Format, interface IWMReaderTimecode
- Formato de sistema avançado (ASF), interface IWMReaderTimecode
- ASF (formato de sistemas avançados), interface IWMReaderTimecode
- Códigos de tempo SMPTE, sobre
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498984"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="526ea-111">Suporte ao código de tempo SMPTE</span><span class="sxs-lookup"><span data-stu-id="526ea-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="526ea-112">O Windows Media Format SDK fornece suporte limitado para o código de tempo SMPTE, que é um formato de código de hora padrão para filmes e televisão.</span><span class="sxs-lookup"><span data-stu-id="526ea-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="526ea-113">Você pode incluir dados de código de tempo SMPTE com exemplos como extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="526ea-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="526ea-114">A parte de dados da extensão é uma estrutura de [**\_ dados de \_ extensão \_ do código**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) de tempo WMT que contém as informações do carimbo de data/hora SMPTE original.</span><span class="sxs-lookup"><span data-stu-id="526ea-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="526ea-115">Manter o código de tempo SMPTE em seus arquivos ASF vem com limites de desempenho.</span><span class="sxs-lookup"><span data-stu-id="526ea-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="526ea-116">Cada exemplo com um carimbo de data/hora SMPTE associado requer o transporte dos 14 bytes na estrutura de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="526ea-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="526ea-117">Em um cenário de streaming, esse maior requisito de largura de banda pode ser catastrófico.</span><span class="sxs-lookup"><span data-stu-id="526ea-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="526ea-118">Como resultado, é recomendável que os códigos de tempo SMPTE só sejam mantidos em arquivos ASF durante o processo de edição de vídeo, que normalmente é feito com arquivos locais.</span><span class="sxs-lookup"><span data-stu-id="526ea-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="526ea-119">Quando o arquivo final for criado, você deverá remover as extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="526ea-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="526ea-120">Você pode ler carimbos de data/hora SMPTE da mesma forma que você lê qualquer outra extensão de unidade de dados, mas os objetos de leitura fornecem suporte integrado para pesquisa por código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="526ea-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="526ea-121">Para poder Pesquisar carimbos de data/hora SMPTE, você deve primeiro indexar o arquivo pelo código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="526ea-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="526ea-122">Você pode configurar o indexador para indexar os códigos de tempo usando o método [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .</span><span class="sxs-lookup"><span data-stu-id="526ea-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="526ea-123">Usando o leitor assíncrono, você pode navegar por um arquivo em carimbos de data/hora do SMPTE usando os métodos da interface [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) e o método [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) .</span><span class="sxs-lookup"><span data-stu-id="526ea-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="526ea-124">Com o leitor síncrono, use [**IWMSyncReader2:: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span><span class="sxs-lookup"><span data-stu-id="526ea-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="526ea-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="526ea-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="526ea-126">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="526ea-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="526ea-127">**Configurar extensões de unidade de dados**</span><span class="sxs-lookup"><span data-stu-id="526ea-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




