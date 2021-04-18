---
description: Usando o Windows Media no DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Usando o Windows Media no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104370820"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="3397c-103">Usando o Windows Media no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3397c-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="3397c-104">Esta seção descreve como usar o DirectShow para reproduzir e gravar arquivos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="3397c-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="3397c-105">Normalmente, os arquivos ASF contêm conteúdo de áudio e vídeo codificado usando os codecs de áudio e vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3397c-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="3397c-106">No entanto, o ASF pode conter qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3397c-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="3397c-107">Os seguintes filtros do DirectShow dão suporte à leitura e gravação de arquivos ASF:</span><span class="sxs-lookup"><span data-stu-id="3397c-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="3397c-108">[Filtro de leitor ASF do WM](wm-asf-reader-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3397c-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="3397c-109">Lê arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="3397c-109">Reads ASF files.</span></span>
-   <span data-ttu-id="3397c-110">[Filtro de gravador ASF do WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3397c-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="3397c-111">Arquivos ASF Wrties.</span><span class="sxs-lookup"><span data-stu-id="3397c-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="3397c-112">[Filtro de invólucro de DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3397c-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="3397c-113">Encapsula o codificador do Windows Media e o decodificador DMOs.</span><span class="sxs-lookup"><span data-stu-id="3397c-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="3397c-114">Versões</span><span class="sxs-lookup"><span data-stu-id="3397c-114">Versions</span></span>

<span data-ttu-id="3397c-115">Os filtros do gravador ASF do WM e do escritor ASF do WM são empacotados na DLL chamada qasf.dll e os filtros são coletivamente nomeados "componentes QASF".</span><span class="sxs-lookup"><span data-stu-id="3397c-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="3397c-116">Esses filtros são wrappers para o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3397c-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="3397c-117">A DLL (qasf.dll) foi publicada pela primeira vez no SDK do DirectX, mas foi atualizada posteriormente no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="3397c-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="3397c-118">Este é o histórico de versão dos filtros QASF:</span><span class="sxs-lookup"><span data-stu-id="3397c-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="3397c-119">O DirectShow 8,1 dá suporte à versão 7,0 do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3397c-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="3397c-120">O DirectShow 9,0 dá suporte à versão 7,1 do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3397c-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="3397c-121">O Windows XP Service Pack 2 dá suporte ao SDK do Windows Media Format 9.</span><span class="sxs-lookup"><span data-stu-id="3397c-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="3397c-122">O Windows Vista dá suporte ao SDK do Windows Media Format 11.</span><span class="sxs-lookup"><span data-stu-id="3397c-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="3397c-123">O SDK do Windows Media Format 9 e posterior contém versões correspondentes do QASF.</span><span class="sxs-lookup"><span data-stu-id="3397c-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="3397c-124">Para obter a versão mais recente do QASF, sempre Baixe o SDK do Windows Media Format mais recente.</span><span class="sxs-lookup"><span data-stu-id="3397c-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="3397c-125">Filtro de origem de mídia do Windows herdado</span><span class="sxs-lookup"><span data-stu-id="3397c-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="3397c-126">No Windows XP Service Pack 1 e versões anteriores, o filtro de origem padrão para arquivos ASF (. ASF,. wmv e extensões de arquivo. WMA) é o [filtro de origem de mídia do Windows](windows-media-source-filter.md)obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3397c-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="3397c-127">Esse comportamento foi mantido para garantir a compatibilidade com versões anteriores com aplicativos que usavam o Windows Media Player 6,4.</span><span class="sxs-lookup"><span data-stu-id="3397c-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="3397c-128">Novos aplicativos devem usar as versões mais recentes do QASF, que tornam o filtro de leitor ASF do WM o filtro padrão para a reprodução de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="3397c-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="3397c-129">Para obter mais informações sobre o Windows Media Suite dos kits de desenvolvimento de software, consulte a seção [áudio e vídeo](../audio-and-video.md) da biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="3397c-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="3397c-130">Este artigo contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3397c-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="3397c-131">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3397c-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="3397c-132">Criando arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3397c-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="3397c-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3397c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3397c-134">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="3397c-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
