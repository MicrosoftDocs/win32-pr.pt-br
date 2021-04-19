---
title: Propriedade ListeningTip
description: Propriedade ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105797557"
---
# <a name="listeningtip-property"></a><span data-ttu-id="ac21a-103">Propriedade ListeningTip</span><span class="sxs-lookup"><span data-stu-id="ac21a-103">ListeningTip Property</span></span>

<span data-ttu-id="ac21a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ac21a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ac21a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="ac21a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ac21a-106">Retorna um valor booleano que indica a configuração de usuário atual para a dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="ac21a-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="ac21a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="ac21a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="ac21a-108">*Agent \* \* *. SpeechInput.ListeningTip**</span><span class="sxs-lookup"><span data-stu-id="ac21a-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="ac21a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="ac21a-109">Value</span></span>     | <span data-ttu-id="ac21a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac21a-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="ac21a-111">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="ac21a-111">**True**</span></span>  | <span data-ttu-id="ac21a-112">A dica de escuta está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ac21a-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="ac21a-113">**Falso**</span><span class="sxs-lookup"><span data-stu-id="ac21a-113">**False**</span></span> | <span data-ttu-id="ac21a-114">A dica de escuta está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="ac21a-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac21a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac21a-115">Remarks</span></span>

<span data-ttu-id="ac21a-116">A propriedade **ListeningTip** indica se a opção Exibir dica de escuta na folha de propriedades do Microsoft Agent (opções avançadas de caracteres) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ac21a-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="ac21a-117">Quando **ListeningTip** retorna **true** e a entrada de fala está habilitada, o servidor exibe a janela de gorjeta quando o usuário pressiona a tecla de escuta.</span><span class="sxs-lookup"><span data-stu-id="ac21a-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac21a-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ac21a-118">See Also</span></span>

[<span data-ttu-id="ac21a-119">**Evento AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="ac21a-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




