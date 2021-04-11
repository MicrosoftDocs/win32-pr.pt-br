---
description: Resolvedor de origem
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Resolvedor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296525"
---
# <a name="source-resolver"></a><span data-ttu-id="320d0-103">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="320d0-103">Source Resolver</span></span>

<span data-ttu-id="320d0-104">O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo.</span><span class="sxs-lookup"><span data-stu-id="320d0-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="320d0-105">O resolvedor de origem é o modo padrão para os aplicativos criarem origens de mídia.</span><span class="sxs-lookup"><span data-stu-id="320d0-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="320d0-106">Internamente, o resolvedor de origem usa objetos de *manipuladores* :</span><span class="sxs-lookup"><span data-stu-id="320d0-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="320d0-107">Os *manipuladores de esquema* usam uma URL e criam uma origem de mídia ou um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="320d0-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="320d0-108">Os *manipuladores de fluxo de bytes* usam um fluxo de bytes e criam uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="320d0-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="320d0-109">Você pode implementar um manipulador personalizado e adicioná-lo ao registro.</span><span class="sxs-lookup"><span data-stu-id="320d0-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="320d0-110">Os manipuladores de esquema são registrados pelo esquema de URL e os manipuladores de fluxo de bytes são registrados por extensão de nome de arquivo ou tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="320d0-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="320d0-111">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="320d0-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="320d0-112">Usando o resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="320d0-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="320d0-113">Configurando uma origem de mídia</span><span class="sxs-lookup"><span data-stu-id="320d0-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="320d0-114">Manipuladores de esquema e manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="320d0-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="320d0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="320d0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="320d0-116">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="320d0-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



