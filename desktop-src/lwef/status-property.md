---
title: Propriedade de status
description: Propriedade de status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765772"
---
# <a name="status-property"></a><span data-ttu-id="c1da2-103">Propriedade de status</span><span class="sxs-lookup"><span data-stu-id="c1da2-103">Status Property</span></span>

<span data-ttu-id="c1da2-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1da2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c1da2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="c1da2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c1da2-106">Retorna o status do canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="c1da2-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="c1da2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="c1da2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c1da2-108">*Agent \* \* *. AudioOutput. status**</span><span class="sxs-lookup"><span data-stu-id="c1da2-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="c1da2-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c1da2-109">Value</span></span> | <span data-ttu-id="c1da2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1da2-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1da2-111">0</span><span class="sxs-lookup"><span data-stu-id="c1da2-111">0</span></span>     | <span data-ttu-id="c1da2-112">O canal de saída de áudio está disponível (não ocupado).</span><span class="sxs-lookup"><span data-stu-id="c1da2-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="c1da2-113">1</span><span class="sxs-lookup"><span data-stu-id="c1da2-113">1</span></span>     | <span data-ttu-id="c1da2-114">Não há suporte para saída de áudio; por exemplo, como não há placa de som.</span><span class="sxs-lookup"><span data-stu-id="c1da2-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="c1da2-115">2</span><span class="sxs-lookup"><span data-stu-id="c1da2-115">2</span></span>     | <span data-ttu-id="c1da2-116">O canal de saída de áudio não pode ser aberto (está ocupado); por exemplo, como algum outro aplicativo está reproduzindo áudio.</span><span class="sxs-lookup"><span data-stu-id="c1da2-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="c1da2-117">3</span><span class="sxs-lookup"><span data-stu-id="c1da2-117">3</span></span>     | <span data-ttu-id="c1da2-118">O canal de saída de áudio está ocupado porque o servidor está processando a entrada de fala do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1da2-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="c1da2-119">4</span><span class="sxs-lookup"><span data-stu-id="c1da2-119">4</span></span>     | <span data-ttu-id="c1da2-120">O canal de saída de áudio está ocupado porque um caractere está falando no momento.</span><span class="sxs-lookup"><span data-stu-id="c1da2-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="c1da2-121">5</span><span class="sxs-lookup"><span data-stu-id="c1da2-121">5</span></span>     | <span data-ttu-id="c1da2-122">O canal de saída de áudio não está ocupado, mas está aguardando a entrada de fala do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1da2-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="c1da2-123">6</span><span class="sxs-lookup"><span data-stu-id="c1da2-123">6</span></span>     | <span data-ttu-id="c1da2-124">Houve algum outro problema (desconhecido) ao tentar acessar o canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="c1da2-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1da2-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1da2-125">Remarks</span></span>

<span data-ttu-id="c1da2-126">Essa configuração permite que o aplicativo cliente consulte o canal de saída de áudio, retornando um valor inteiro que indica o status do canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="c1da2-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="c1da2-127">Você pode usar isso para determinar se é apropriado que seu caractere fale ou se é apropriado tentar ativar o modo de escuta (usando o método [**Listen**](listen-method.md) ).</span><span class="sxs-lookup"><span data-stu-id="c1da2-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1da2-128">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c1da2-128">See Also</span></span>

[<span data-ttu-id="c1da2-129">**Evento ListenComplete**</span><span class="sxs-lookup"><span data-stu-id="c1da2-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




