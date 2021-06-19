---
description: Saiba mais sobre como criar arquivos ASF no DirectShow. ASF é um formato de contêiner que pode conter qualquer tipo de dados.
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Criando arquivos ASF no DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4614ed813c2e9f51c77cd8773739188aa5d4d07
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403960"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="70942-104">Criando arquivos ASF no DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="70942-104">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="70942-105">Esta seção descreve como usar o filtro DirectShow [WM ASF Writer](wm-asf-writer-filter.md) para criar arquivos no ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="70942-105">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="70942-106">ASF é um formato de contêiner que pode conter qualquer tipo de dados compactados ou descompactados.</span><span class="sxs-lookup"><span data-stu-id="70942-106">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="70942-107">Windows Media Format arquivos são arquivos ASF que usam determinados codecs, conforme especificado no SDK (Software Development Kit) do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="70942-107">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="70942-108">Esses arquivos usam as extensões ".wma" para arquivos de Áudio de Mídia do Windows e ".wmv" para arquivos de Vídeo de Mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="70942-108">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="70942-109">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="70942-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="70942-110">O SDK do DirectShow e o Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="70942-110">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="70942-111">Configurando o asf writer</span><span class="sxs-lookup"><span data-stu-id="70942-111">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="70942-112">Criando grafos de filtro para gravar arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="70942-112">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="70942-113">Configurar perfis e outras propriedades de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="70942-113">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="70942-114">Desbloqueando o Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="70942-114">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="70942-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70942-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70942-116">Usando a Mídia do Windows no DirectShow</span><span class="sxs-lookup"><span data-stu-id="70942-116">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



