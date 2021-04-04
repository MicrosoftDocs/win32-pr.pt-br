---
title: Sobre manipuladores de arquivo e fluxo personalizados
description: Sobre manipuladores de arquivo e fluxo personalizados
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
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
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823018"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="b3cf5-111">Sobre manipuladores de arquivo e fluxo personalizados</span><span class="sxs-lookup"><span data-stu-id="b3cf5-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="b3cf5-112">Seu aplicativo pode usar um manipulador de arquivo personalizado para ler de um arquivo ou gravar em um arquivo que esteja em um formato não padrão.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="b3cf5-113">Para fazer isso, seu aplicativo simplesmente usa o nome do manipulador de arquivo ao abrir o arquivo ou alocar a interface de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="b3cf5-114">Em seguida, a biblioteca AVIFile usa as funções do manipulador de arquivos, em vez daquelas de outro manipulador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="b3cf5-115">O formato não padrão aparece como dados AVI padrão para seu aplicativo ou para qualquer outro aplicativo usando seu manipulador de arquivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="b3cf5-116">Da mesma forma, seu aplicativo pode usar um manipulador de fluxo personalizado para ler um fluxo que está em um formato não padrão.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="b3cf5-117">Um fluxo — se ele constitui áudio, vídeo, MIDI, texto ou dados personalizados — é um componente de um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="b3cf5-118">Por exemplo, um arquivo AVI que contém uma sequência de vídeo, uma trilha sonora em inglês e uma trilha sonora francesa consiste em três fluxos.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="b3cf5-119">Seu aplicativo pode especificar os fluxos em um arquivo AVI para processar e direcionar cada um desses fluxos para um manipulador que pode processar de forma ideal o tipo apropriado de dados de multimídia.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="b3cf5-120">Você deve posicionar os manipuladores de arquivo e fluxo personalizados em uma ou mais DLLs, separadas dos arquivos principais do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b3cf5-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




