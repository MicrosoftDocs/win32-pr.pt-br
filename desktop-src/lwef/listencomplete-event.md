---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364358"
---
# <a name="listencomplete-event"></a><span data-ttu-id="b04b1-103">Evento ListenComplete</span><span class="sxs-lookup"><span data-stu-id="b04b1-103">ListenComplete Event</span></span>

<span data-ttu-id="b04b1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b04b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b04b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="b04b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b04b1-106">Ocorre quando o modo de escuta (reconhecimento de fala) termina.</span><span class="sxs-lookup"><span data-stu-id="b04b1-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="b04b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b04b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b04b1-108">**Sub** *Agent. \* \* \* ListenComplete (ByVal* \*  *characterid*, **ByVal** *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="b04b1-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="b04b1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b04b1-109">Part</span></span>          | <span data-ttu-id="b04b1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b04b1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04b1-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="b04b1-111">*CharacterID*</span></span> | <span data-ttu-id="b04b1-112">Retorna a ID do caractere de escuta como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b04b1-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b04b1-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="b04b1-113">*Cause*</span></span>       | <span data-ttu-id="b04b1-114">Retorna a causa do evento complete como um inteiro que pode ser um dos seguintes: 1 modo de escuta foi desativado pelo código do programa.</span><span class="sxs-lookup"><span data-stu-id="b04b1-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="b04b1-115">2 o modo de escuta (ativado pelo código do programa) atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="b04b1-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="b04b1-116">3 o modo de escuta (ativado pela chave de escuta) atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="b04b1-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="b04b1-117">4 o modo de escuta foi desativado porque o usuário liberou a chave de escuta.</span><span class="sxs-lookup"><span data-stu-id="b04b1-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="b04b1-118">5 o modo de escuta terminou porque o usuário terminou de falar.</span><span class="sxs-lookup"><span data-stu-id="b04b1-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="b04b1-119">6 o modo de escuta foi encerrado porque o cliente de entrada-ativo foi desativado.</span><span class="sxs-lookup"><span data-stu-id="b04b1-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="b04b1-120">7 modo de escuta encerrado porque o caractere padrão foi alterado.</span><span class="sxs-lookup"><span data-stu-id="b04b1-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="b04b1-121">8 modo de escuta terminou porque o usuário desabilitou a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="b04b1-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="b04b1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b04b1-122">Remarks</span></span>

<span data-ttu-id="b04b1-123">Esse evento é enviado a todos os clientes quando o tempo limite do modo de escuta termina, depois que o usuário libera a chave de escuta, quando o cliente ativo de entrada chama o método [**Listen**](listen-method.md) com **false** ou o usuário terminou de falar.</span><span class="sxs-lookup"><span data-stu-id="b04b1-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="b04b1-124">Você pode usar esse evento para determinar quando retomar a saída de caractere falado (áudio).</span><span class="sxs-lookup"><span data-stu-id="b04b1-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="b04b1-125">Se você ativar o modo de escuta usando o método [**Listen**](listen-method.md) e, em seguida, o usuário pressionar a tecla de escuta, o modo de escuta redefinirá e continuará até que o tempo limite da chave de escuta seja concluído, a chave de escuta será liberada ou o usuário terminará de falar, o que for mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b04b1-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="b04b1-126">Nessa situação, você não receberá um evento **ListenComplete** até que o modo da chave de escuta seja concluído.</span><span class="sxs-lookup"><span data-stu-id="b04b1-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="b04b1-127">O evento retorna o caractere para os clientes que atualmente têm esse caractere carregado.</span><span class="sxs-lookup"><span data-stu-id="b04b1-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="b04b1-128">Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="b04b1-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="b04b1-129">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b04b1-129">See Also</span></span>

<span data-ttu-id="b04b1-130">[**Evento ListenStart**](listenstart-event.md), [ **método Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="b04b1-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





