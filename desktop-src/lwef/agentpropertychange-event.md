---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005300"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="d1138-103">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="d1138-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="d1138-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1138-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d1138-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="d1138-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d1138-106">Ocorre quando o usuário altera uma propriedade na janela Opções de caractere avançadas.</span><span class="sxs-lookup"><span data-stu-id="d1138-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="d1138-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="d1138-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d1138-108">**Sub** - *agente. \* \* \* AgentPropertyChange*\*</span><span class="sxs-lookup"><span data-stu-id="d1138-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="d1138-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1138-109">Remarks</span></span>

<span data-ttu-id="d1138-110">Esse evento indica quando o usuário alterou e aplicou qualquer propriedade incluída na janela de opção de caractere avançado.</span><span class="sxs-lookup"><span data-stu-id="d1138-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="d1138-111">No seu código para tratar esse evento, você pode consultar as configurações de propriedade específicas dos objetos [AudioOutput](the-audiooutput-object.md) ou [SpeechInput](the-speechinput-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d1138-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="d1138-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d1138-112">See Also</span></span>

[<span data-ttu-id="d1138-113">**Evento DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="d1138-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




