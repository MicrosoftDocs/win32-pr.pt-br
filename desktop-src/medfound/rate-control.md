---
description: Controle de taxa
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: Controle de taxa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787686"
---
# <a name="rate-control"></a><span data-ttu-id="626fc-103">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="626fc-103">Rate Control</span></span>

<span data-ttu-id="626fc-104">A [sessão de mídia](media-session.md) dá suporte à alteração da taxa de reprodução, que um aplicativo pode usar para implementar recursos de reprodução, como avançar e retroceder.</span><span class="sxs-lookup"><span data-stu-id="626fc-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="626fc-105">Esta seção descreve como os aplicativos podem alterar a taxa de reprodução ao usar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="626fc-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="626fc-106">Para obter informações sobre como dar suporte ao controle de taxa em seus próprios componentes de pipeline, consulte [implementando o controle de taxa](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="626fc-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="626fc-107">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="626fc-107">This section contains the following topics.</span></span>



| <span data-ttu-id="626fc-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="626fc-108">Topic</span></span>                                                                                                      | <span data-ttu-id="626fc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="626fc-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="626fc-110">Sobre o controle de taxa</span><span class="sxs-lookup"><span data-stu-id="626fc-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="626fc-111">Fornece uma visão geral do controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="626fc-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="626fc-112">Como determinar as taxas com suporte</span><span class="sxs-lookup"><span data-stu-id="626fc-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="626fc-113">Como encontrar as taxas de reprodução com suporte mais rápidas e mais lentas.</span><span class="sxs-lookup"><span data-stu-id="626fc-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="626fc-114">Como definir a taxa de reprodução na sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="626fc-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="626fc-115">Como alterar a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="626fc-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="626fc-116">Como executar a depuração</span><span class="sxs-lookup"><span data-stu-id="626fc-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="626fc-117">Como passar um quadro de vídeo por vez.</span><span class="sxs-lookup"><span data-stu-id="626fc-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="626fc-118">Implementando o controle de taxa</span><span class="sxs-lookup"><span data-stu-id="626fc-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="626fc-119">Como dar suporte a taxas de reprodução de variáveis em um componente de pipeline personalizado.</span><span class="sxs-lookup"><span data-stu-id="626fc-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="626fc-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="626fc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="626fc-121">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="626fc-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="626fc-122">Busca, avanço rápido e reprodução reversa</span><span class="sxs-lookup"><span data-stu-id="626fc-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



