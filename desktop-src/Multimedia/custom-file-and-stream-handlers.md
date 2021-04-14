---
title: Manipuladores de arquivo e fluxo personalizados
description: Manipuladores de arquivo e fluxo personalizados
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Video for Windows (VFW), manipuladores de arquivo personalizado
- Vídeo para Windows (VFW), manipuladores de fluxo personalizados
- Video for Windows (VFW), manipuladores de arquivos
- Vídeo para Windows (VFW), manipuladores de fluxo
- VFW (vídeo para Windows), manipuladores de arquivo personalizado
- VFW (vídeo para Windows), manipuladores de fluxo personalizados
- VFW (vídeo para Windows), manipuladores de arquivo
- VFW (vídeo para Windows), manipuladores de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453639"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="bfdff-111">Manipuladores de arquivo e fluxo personalizados</span><span class="sxs-lookup"><span data-stu-id="bfdff-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="bfdff-112">Manipuladores de arquivo e fluxo são drivers que fornecem interfaces consistentes a um aplicativo que controla dados de multimídia.</span><span class="sxs-lookup"><span data-stu-id="bfdff-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="bfdff-113">Os manipuladores de arquivo e de fluxo incluídos no sistema operacional usam dados de vídeo e de formato de onda de áudio armazenados em arquivos AVI (áudio-video intercalado) e Wave-Audio.</span><span class="sxs-lookup"><span data-stu-id="bfdff-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="bfdff-114">Você pode escrever manipuladores para permitir que seu aplicativo grave ou acesse dados de multimídia de outra fonte, como um arquivo usando um formato proprietário, um arquivo AVI que foi expandido para conter fluxos de dados adicionais ou um manipulador que gera seus próprios dados de multimídia.</span><span class="sxs-lookup"><span data-stu-id="bfdff-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="bfdff-115">Se você tiver um formato de arquivo personalizado para dados AVI que deseja usar com as [funções e macros do avifile](avifile-functions-and-macros.md), precisará escrever um manipulador personalizado.</span><span class="sxs-lookup"><span data-stu-id="bfdff-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="bfdff-116">Sobre manipuladores de arquivo e fluxo personalizados</span><span class="sxs-lookup"><span data-stu-id="bfdff-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="bfdff-117">Usando manipuladores de arquivo e fluxo personalizados</span><span class="sxs-lookup"><span data-stu-id="bfdff-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="bfdff-118">Referência de manipulador de arquivo e fluxo personalizado</span><span class="sxs-lookup"><span data-stu-id="bfdff-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 




