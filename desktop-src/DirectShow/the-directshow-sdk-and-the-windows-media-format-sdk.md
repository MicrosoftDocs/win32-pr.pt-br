---
description: O SDK do DirectShow e o Windows Media Format SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: O SDK do DirectShow e o Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297981"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="2c4e8-103">O SDK do DirectShow e o Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="2c4e8-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="2c4e8-104">O DirectShow e o Windows Media Format SDK oferecem soluções complementares para a gravação de aplicativos que criam e reproduzem fluxos de formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="2c4e8-105">Para obter mais informações, consulte a seção "[áudio e vídeo](../audio-and-video.md)" da biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="2c4e8-106">O filtro do gravador ASF aceita qualquer número de fluxos de entrada e cria um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="2c4e8-107">O filtro usa o Windows Media Format SDK para converter arquivos de áudio ou vídeo não compactados em conteúdo baseado no Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="2c4e8-108">O conteúdo compactado é armazenado no formato de contêiner ASF.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="2c4e8-109">Se o conteúdo for somente áudio, o arquivo receberá uma extensão. WMA e será chamado de arquivo de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="2c4e8-110">Se o conteúdo for somente vídeo ou vídeo e áudio, o arquivo receberá uma extensão. wmv e será chamado de arquivo de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="2c4e8-111">Qualquer um dos tipos de arquivo também pode incluir metadados.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="2c4e8-112">Você pode usar o gravador ASF do WM em vários cenários, incluindo captura Audio-Video de vídeo digital (DV), recompactação de áudio e conversão de arquivos multimídia intercalados (AVI) ou MPEG para transmissão de rede.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="2c4e8-113">Esse filtro fornece a única maneira de criar arquivos do Microsoft® Windows Media™ Audio (WMA) e do Windows Media Video (WMV) no DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="2c4e8-114">O filtro também pode criar arquivos protegidos por DRM (Rights Management digital) e também pode criar conteúdo MPEG-4 usando o codificador MPEG-4 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="2c4e8-115">Esse conteúdo é armazenado no formato de contêiner ASF.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c4e8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c4e8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c4e8-117">Criando arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="2c4e8-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
