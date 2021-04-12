---
description: Trabalhando com vídeo
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: Trabalhando com vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297394"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="3b196-103">Trabalhando com vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="3b196-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="3b196-104">Embora os codecs de vídeo individuais tenham suas próprias peculiaridades, todos usam os mesmos procedimentos básicos.</span><span class="sxs-lookup"><span data-stu-id="3b196-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="3b196-105">Esta seção descreve como codificar e decodificar vídeos com os codecs de vídeo do Windows Media e resolve os recursos específicos de cada um.</span><span class="sxs-lookup"><span data-stu-id="3b196-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="3b196-106">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="3b196-106">This section contains the following topics.</span></span>



| <span data-ttu-id="3b196-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="3b196-107">Topic</span></span>                                                                                                        | <span data-ttu-id="3b196-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b196-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b196-109">Escolhendo um codec de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b196-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="3b196-110">Descreve os tipos de conteúdo mais adequados para compactação com cada um dos codecs de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3b196-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="3b196-111">Configurando a codificação de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b196-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="3b196-112">Descreve como configurar o codificador de vídeo DMOs.</span><span class="sxs-lookup"><span data-stu-id="3b196-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="3b196-113">Configurando decodificação de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b196-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="3b196-114">Descreve como configurar o DMOs do decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b196-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="3b196-115">Inserção de quadro-chave forçada</span><span class="sxs-lookup"><span data-stu-id="3b196-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="3b196-116">Descreve como solicitar que um exemplo seja codificado como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="3b196-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="3b196-117">Codificação de vídeo entrelaçado</span><span class="sxs-lookup"><span data-stu-id="3b196-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="3b196-118">Descreve como manter o entrelaçamento em fluxos de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3b196-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="3b196-119">Usando o codec de perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3b196-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="3b196-120">Descreve como usar o codec de perfil avançado do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="3b196-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="3b196-121">Usando o codec de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3b196-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="3b196-122">Descreve como usar o codec de tela do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="3b196-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="3b196-123">Usando o codec de imagem do Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="3b196-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="3b196-124">Descreve como usar o codec de imagem do Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="3b196-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="3b196-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b196-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b196-126">Codificações de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="3b196-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



