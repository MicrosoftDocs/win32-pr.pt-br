---
description: Configurando decodificação de vídeo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configurando a decodificação de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782388"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="0c278-103">Configurando a decodificação de vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="0c278-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="0c278-104">A decodificação é essencialmente o oposto da codificação em termos de configuração.</span><span class="sxs-lookup"><span data-stu-id="0c278-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="0c278-105">O decodificador dá suporte a poucas propriedades, e nenhuma delas é necessária.</span><span class="sxs-lookup"><span data-stu-id="0c278-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="0c278-106">Defina o tipo de entrada para o tipo usado para a saída do decodificador (incluindo os dados privados do codec).</span><span class="sxs-lookup"><span data-stu-id="0c278-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="0c278-107">Em seguida, defina a saída para o formato descompactado desejado, defina a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para refletir o tamanho do quadro apropriado e comece a processar exemplos.</span><span class="sxs-lookup"><span data-stu-id="0c278-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="0c278-108">Você deve fornecer o decodificador com um tipo de mídia que inclua os dados privados do codec posicionados imediatamente após a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="0c278-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="0c278-109">O decodificador não pode decodificar o conteúdo sem esses dados.</span><span class="sxs-lookup"><span data-stu-id="0c278-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="0c278-110">A validação de formato executada pelo decodificador não valida os dados privados.</span><span class="sxs-lookup"><span data-stu-id="0c278-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="0c278-111">Se os dados privados do codec estiverem ausentes ou incorretos, o decodificador responderá como se o fluxo de bits estiver corrompido.</span><span class="sxs-lookup"><span data-stu-id="0c278-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="0c278-112">Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="0c278-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c278-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c278-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c278-114">Usando dados privados do codec de vídeo</span><span class="sxs-lookup"><span data-stu-id="0c278-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="0c278-115">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="0c278-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
