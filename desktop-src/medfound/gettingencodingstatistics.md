---
description: Descreve as estatísticas que você pode recuperar de um codec do Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtendo estatísticas de codificação (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646579"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="eed3a-103">Obtendo estatísticas de codificação (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="eed3a-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="eed3a-104">As informações sobre o que está acontecendo em uma sessão de codificação geralmente estão imediatamente disponíveis na forma de códigos de erro retornados durante o processamento de amostras.</span><span class="sxs-lookup"><span data-stu-id="eed3a-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="eed3a-105">No entanto, há algumas estatísticas que você pode recuperar do codec sobre vários aspectos de codificação.</span><span class="sxs-lookup"><span data-stu-id="eed3a-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="eed3a-106">Informações de quadro de vídeo</span><span class="sxs-lookup"><span data-stu-id="eed3a-106">Video Frame Information</span></span>

<span data-ttu-id="eed3a-107">Algumas estatísticas de vídeo que você pode recuperar tratam do número de quadros processados pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="eed3a-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="eed3a-108">Há três propriedades de número de quadro que você pode ler do codificador de vídeo:</span><span class="sxs-lookup"><span data-stu-id="eed3a-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="eed3a-109">[MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) é o número de quadros processados por meio do fluxo de entrada do DMO.</span><span class="sxs-lookup"><span data-stu-id="eed3a-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="eed3a-110">[MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) é o número de quadros codificados.</span><span class="sxs-lookup"><span data-stu-id="eed3a-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="eed3a-111">Ao subtrair esse valor do número total de quadros passados, você pode determinar quantos quadros foram descartados.</span><span class="sxs-lookup"><span data-stu-id="eed3a-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="eed3a-112">[MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) é o número de quadros não codificados porque eles duplicaram o conteúdo já incluído.</span><span class="sxs-lookup"><span data-stu-id="eed3a-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="eed3a-113">Esse valor não é subtraído do número de quadros codificados relatados pelo DMO.</span><span class="sxs-lookup"><span data-stu-id="eed3a-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="eed3a-114">Você pode ler as propriedades do quadro de vídeo a qualquer momento durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="eed3a-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="eed3a-115">Isso pode ser útil para determinar se as configurações de codificação são apropriadas para o seu conteúdo; Se houver uma grande diferença entre os quadros totais e os quadros codificados, o conteúdo compactado poderá não atender aos seus requisitos de qualidade.</span><span class="sxs-lookup"><span data-stu-id="eed3a-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="eed3a-116">Você pode ler os valores finais depois de concluir a codificação.</span><span class="sxs-lookup"><span data-stu-id="eed3a-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="eed3a-117">Estatísticas de buffer de VBR</span><span class="sxs-lookup"><span data-stu-id="eed3a-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="eed3a-118">Dependendo do modo de codificação usado, algumas ou todas as configurações de buffer podem ser determinadas durante a codificação (por exemplo, a taxa de bits de VBR com base na qualidade não é conhecida até que o conteúdo seja codificado).</span><span class="sxs-lookup"><span data-stu-id="eed3a-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="eed3a-119">Há quatro propriedades de buffer de VBR que você pode obter usando o método **IPropertyBag:: Read** :</span><span class="sxs-lookup"><span data-stu-id="eed3a-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="eed3a-120">[MFPKEY \_ RAVG](mfpkey-ravgproperty.md) é a taxa de bits média do conteúdo da VBR.</span><span class="sxs-lookup"><span data-stu-id="eed3a-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="eed3a-121">[MFPKEY \_ BAVG](mfpkey-bavgproperty.md) é a janela de buffer para a taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="eed3a-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="eed3a-122">[MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) é a taxa de bits de pico do conteúdo da VBR.</span><span class="sxs-lookup"><span data-stu-id="eed3a-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="eed3a-123">[MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) é a janela de buffer de pico.</span><span class="sxs-lookup"><span data-stu-id="eed3a-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="eed3a-124">Depois de começar a processar os exemplos, você não deve ler nenhuma das propriedades de VBR até concluir a codificação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="eed3a-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="eed3a-125">Se você fizer isso, o codificador interpretará sua solicitação como um sinal de que a codificação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="eed3a-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="eed3a-126">O próximo exemplo que você processa é tratado como uma nova sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="eed3a-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eed3a-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eed3a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed3a-128">Codificações de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="eed3a-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



