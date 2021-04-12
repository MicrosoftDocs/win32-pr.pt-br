---
description: Vantagens do streaming de multimídia
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vantagens do streaming de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091875"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="15617-103">Vantagens do streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="15617-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="15617-104">Essas APIs são preteridas.</span><span class="sxs-lookup"><span data-stu-id="15617-104">These APIs are deprecated.</span></span> <span data-ttu-id="15617-105">Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="15617-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="15617-106">Quando os desenvolvedores usam o streaming de multimídia em seus aplicativos, reduz consideravelmente a quantidade de programação específica de formato necessária.</span><span class="sxs-lookup"><span data-stu-id="15617-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="15617-107">Normalmente, um aplicativo que deve obter dados de mídia de uma fonte de arquivo ou de hardware deve saber tudo sobre o formato de dados e o dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="15617-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="15617-108">O aplicativo deve lidar com a conexão, a transferência de dados, qualquer conversão de dados necessária e o armazenamento de arquivos ou processamento de dados real.</span><span class="sxs-lookup"><span data-stu-id="15617-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="15617-109">Como cada formato e dispositivo é ligeiramente diferente, esse processo geralmente é complexo e complicado.</span><span class="sxs-lookup"><span data-stu-id="15617-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="15617-110">O streaming de multimídia, por outro lado, negocia automaticamente a transferência e a conversão de dados da origem para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15617-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="15617-111">As interfaces de streaming fornecem um método uniforme e previsível de acesso e controle de dados, o que torna mais fácil para um aplicativo reproduzir os dados, independentemente de sua origem ou formato original.</span><span class="sxs-lookup"><span data-stu-id="15617-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="15617-112">As etapas a seguir mostram como implementar o streaming, do dispositivo de hardware para a reprodução renderizada.</span><span class="sxs-lookup"><span data-stu-id="15617-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="15617-113">Uma fonte de dados de vídeo, como o DirectShow, expõe as interfaces de streaming.</span><span class="sxs-lookup"><span data-stu-id="15617-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="15617-114">O desenvolvedor de aplicativos usa as interfaces de streaming de multimídia para manipular a conversão de formato de dados.</span><span class="sxs-lookup"><span data-stu-id="15617-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="15617-115">O desenvolvedor do aplicativo usa as interfaces do DirectDraw para renderizar os dados resultantes.</span><span class="sxs-lookup"><span data-stu-id="15617-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="15617-116">A especificação para fluxos de multimídia abrange várias interfaces; cada interface inclui métodos que controlam um determinado aspecto do processo de streaming ou lidam com um determinado tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="15617-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="15617-117">Confira a [lista de interfaces de streaming de multimídia](list-of-multimedia-streaming-interfaces.md) para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="15617-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15617-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15617-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15617-119">Sobre a arquitetura de streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="15617-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



