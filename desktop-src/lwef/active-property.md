---
title: Propriedade ativa
description: Propriedade ativa
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159807"
---
# <a name="active-property"></a><span data-ttu-id="aad52-103">Propriedade ativa</span><span class="sxs-lookup"><span data-stu-id="aad52-103">Active Property</span></span>

<span data-ttu-id="aad52-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aad52-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="aad52-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="aad52-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="aad52-106">Retorna se seu aplicativo é o cliente ativo do caractere e se o caractere está no nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="aad52-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="aad52-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="aad52-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="aad52-108">\*agente do. ***Caracteres \* \* \* \* ("*** characterid \* \* *").* \*  \[  =  *Estado* ativo\]</span><span class="sxs-lookup"><span data-stu-id="aad52-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="aad52-109">Parte</span><span class="sxs-lookup"><span data-stu-id="aad52-109">Part</span></span>    | <span data-ttu-id="aad52-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="aad52-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad52-111">*state*</span><span class="sxs-lookup"><span data-stu-id="aad52-111">*state*</span></span> | <span data-ttu-id="aad52-112">Uma expressão de inteiro que especifica o estado do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="aad52-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="aad52-113">0 não é o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="aad52-113">0 Not the active client.</span></span><br/> <span data-ttu-id="aad52-114">1 o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="aad52-114">1 The active client.</span></span> <br/> <span data-ttu-id="aad52-115">2 o cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="aad52-115">2 The input-active client.</span></span> <span data-ttu-id="aad52-116">(O caractere superior).</span><span class="sxs-lookup"><span data-stu-id="aad52-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aad52-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="aad52-117">Remarks</span></span>

<span data-ttu-id="aad52-118">Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, os eventos [**Click**](click-event.md) ou [DragStart](dragstart-event.md) do controle do Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="aad52-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="aad52-119">Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de comando.</span><span class="sxs-lookup"><span data-stu-id="aad52-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="aad52-120">Você pode usar o método [**Activate**](activate-method.md)para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente de entrada ativo (o que também torna o caractere mais alto).</span><span class="sxs-lookup"><span data-stu-id="aad52-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="aad52-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="aad52-121">See Also</span></span>

[<span data-ttu-id="aad52-122">Ativar \* \* método \* \*</span><span class="sxs-lookup"><span data-stu-id="aad52-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





