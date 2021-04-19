---
description: Propriedades de exemplo de MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Propriedades de exemplo de MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810933"
---
# <a name="mpeg-sample-properties"></a><span data-ttu-id="6167e-103">Propriedades de exemplo de MPEG</span><span class="sxs-lookup"><span data-stu-id="6167e-103">MPEG Sample Properties</span></span>

<span data-ttu-id="6167e-104">Exemplos de MPEG têm as seguintes características.</span><span class="sxs-lookup"><span data-stu-id="6167e-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="6167e-105">**Carimbos de Data/Hora**</span><span class="sxs-lookup"><span data-stu-id="6167e-105">**Time Stamps**</span></span>

<span data-ttu-id="6167e-106">Nem todas as amostras têm horários de início e parada.</span><span class="sxs-lookup"><span data-stu-id="6167e-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="6167e-107">O tempo de parada de exemplo para dados de pacote e carga não é útil; Normalmente, ela é definida como a hora de início mais uma.</span><span class="sxs-lookup"><span data-stu-id="6167e-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="6167e-108">Os exemplos de dados de pacote ou de carga MPEG terão um horário de início e de parada definido se o pacote da camada do sistema do qual eles são gerados tiver um PTS válido.</span><span class="sxs-lookup"><span data-stu-id="6167e-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="6167e-109">Para obter mais informações sobre carimbos de data/hora, consulte a seção 2.4.1 de ISO1-11172: "o cabeçalho do pacote pode conter decodificação e/ou carimbos de data/hora (DTS e PTS) que se referem à primeira unidade de acesso no pacote."</span><span class="sxs-lookup"><span data-stu-id="6167e-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="6167e-110">Para \_ tipos principais de fluxo MPEG, a hora de início é a posição de byte do primeiro byte, classificada em 1 byte por segundo.</span><span class="sxs-lookup"><span data-stu-id="6167e-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="6167e-111">A hora de parada é a posição de byte do último byte.</span><span class="sxs-lookup"><span data-stu-id="6167e-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="6167e-112">Portanto, os exemplos consecutivos devem ter a hora de parada do primeiro pacote igual à hora de início do próximo pacote.</span><span class="sxs-lookup"><span data-stu-id="6167e-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="6167e-113">Para dados de CD de vídeo, a origem da mídia deve corresponder ao formato de um arquivo de vídeo-CD exposto por CDFS com a parte padrão do RIFF no início.</span><span class="sxs-lookup"><span data-stu-id="6167e-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="6167e-114">Para os tipos de conteúdo e pacote de vídeo MPEG, o carimbo de data/hora é o tempo de apresentação para o primeiro quadro de vídeo cujo código de início de imagem começa no exemplo.</span><span class="sxs-lookup"><span data-stu-id="6167e-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="6167e-115">Para tipos de carga e pacote de áudio MPEG, o carimbo de data/hora é o tempo de apresentação para o primeiro quadro de áudio cujo código de sincronização começa no exemplo.</span><span class="sxs-lookup"><span data-stu-id="6167e-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="6167e-116">Supõe-se que os dados de pacote e carga sem carimbos de data/hora possam ser registrados com êxito pelos filtros de manipulação.</span><span class="sxs-lookup"><span data-stu-id="6167e-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="6167e-117">**Descontinuidades**</span><span class="sxs-lookup"><span data-stu-id="6167e-117">**Discontinuities**</span></span>

<span data-ttu-id="6167e-118">Se houver uma interrupção no fluxo (por exemplo, uma lacuna nos dados em tempo real ou um erro nos dados ou após uma busca), a propriedade de descontinuidade será definida no exemplo de mídia seguinte.</span><span class="sxs-lookup"><span data-stu-id="6167e-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="6167e-119">Isso também permite uma descontinuidade de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="6167e-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="6167e-120">**Notificações de fim de fluxo**</span><span class="sxs-lookup"><span data-stu-id="6167e-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="6167e-121">Quando o decodificador recebe essa notificação, ele deve processar dados armazenados em buffer.</span><span class="sxs-lookup"><span data-stu-id="6167e-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="6167e-122">Todos os novos dados devem começar com a propriedade de descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="6167e-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6167e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6167e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6167e-124">Suporte a MPEG-2 no DirectShow</span><span class="sxs-lookup"><span data-stu-id="6167e-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



