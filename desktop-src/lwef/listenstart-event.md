---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822954"
---
# <a name="listenstart-event"></a><span data-ttu-id="6ff9a-103">Evento ListenStart</span><span class="sxs-lookup"><span data-stu-id="6ff9a-103">ListenStart Event</span></span>

<span data-ttu-id="6ff9a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ff9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6ff9a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="6ff9a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6ff9a-106">Ocorre quando o modo de escuta (reconhecimento de fala) é iniciado.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="6ff9a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="6ff9a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6ff9a-108">**Sub** *Agent. \* \* \* ListenStart (ByVal* \*  *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="6ff9a-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="6ff9a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6ff9a-109">Part</span></span>          | <span data-ttu-id="6ff9a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ff9a-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="6ff9a-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="6ff9a-111">*CharacterID*</span></span> | <span data-ttu-id="6ff9a-112">Retorna a ID do caractere de escuta como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="6ff9a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ff9a-113">Remarks</span></span>

<span data-ttu-id="6ff9a-114">Esse evento é enviado a todos os clientes quando o modo de escuta começa porque o usuário pressionou a chave de escuta ou o cliente de entrada-ativo chamou o método [**Listen**](listen-method.md) com **true**.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="6ff9a-115">Você pode usar esse evento para evitar que seu caractere fale enquanto o modo de escuta está ativado.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="6ff9a-116">Se você ativar o modo de escuta com o método [**Listen**](listen-method.md) e, em seguida, o usuário pressionar a tecla de escuta, o modo de escuta redefinirá e continuará até que o tempo limite da chave de escuta seja concluído, a chave de escuta será liberada ou o usuário terminará de falar, o que for mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="6ff9a-117">Nessa situação, quando o modo de escuta já estiver ativado, você não receberá um evento **ListenStart** adicional quando o usuário pressionar a tecla de escuta.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="6ff9a-118">O evento retorna o caractere para os clientes que atualmente têm esse caractere carregado.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="6ff9a-119">Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="6ff9a-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="6ff9a-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6ff9a-120">See Also</span></span>

<span data-ttu-id="6ff9a-121">[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="6ff9a-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




