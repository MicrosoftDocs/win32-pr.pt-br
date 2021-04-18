---
description: Criando arquivos ASF no DirectShow
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Criando arquivos ASF no DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f5c9ebac0b14b736c47599ee25a1c1c28dd8f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105756613"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="d06d1-103">Criando arquivos ASF no DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d06d1-103">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="d06d1-104">Esta seção descreve como usar o filtro do [gravador ASF](wm-asf-writer-filter.md) do DirectShow WM para criar arquivos no formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d06d1-104">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="d06d1-105">O ASF é um formato de contêiner que pode conter qualquer tipo de dados compactados ou descompactados.</span><span class="sxs-lookup"><span data-stu-id="d06d1-105">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="d06d1-106">Os arquivos de formato de mídia do Windows são arquivos ASF que usam determinados codecs, conforme especificado no SDK (Software Development Kit) do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d06d1-106">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="d06d1-107">Esses arquivos usam as extensões ". WMA" para arquivos de áudio do Windows Media e ". wmv" para arquivos de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d06d1-107">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="d06d1-108">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="d06d1-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d06d1-109">O SDK do DirectShow e o Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="d06d1-109">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="d06d1-110">Configurando o gravador ASF</span><span class="sxs-lookup"><span data-stu-id="d06d1-110">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="d06d1-111">Criando gráficos de filtro para gravar arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="d06d1-111">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="d06d1-112">Configurar perfis e outras propriedades de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="d06d1-112">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="d06d1-113">Desbloqueando o SDK do Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="d06d1-113">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="d06d1-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d06d1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d06d1-115">Usando o Windows Media no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d06d1-115">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



