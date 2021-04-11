---
title: Propriedade Visible (objeto Balloon)
description: Propriedade Visible
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008669"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="98006-103">Propriedade Visible (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="98006-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="98006-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98006-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="98006-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="98006-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="98006-106">Retorna ou define a configuração visível para o balão de palavra do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="98006-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="98006-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="98006-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="98006-108">\*Agente \***. Caracteres (**"\* characterid \*" \* *). Balão.* \*  \[  =  *booliano* visível\]</span><span class="sxs-lookup"><span data-stu-id="98006-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="98006-109">Parte</span><span class="sxs-lookup"><span data-stu-id="98006-109">Part</span></span>      | <span data-ttu-id="98006-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="98006-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98006-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="98006-111">*boolean*</span></span> | <span data-ttu-id="98006-112">Uma expressão booliana que especifica se o balão de palavra está visível.</span><span class="sxs-lookup"><span data-stu-id="98006-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="98006-113">**Verdadeiro** O balão está visível.</span><span class="sxs-lookup"><span data-stu-id="98006-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="98006-114">**Falso** O balão está oculto.</span><span class="sxs-lookup"><span data-stu-id="98006-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98006-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="98006-115">Remarks</span></span>

<span data-ttu-id="98006-116">Se você seguir uma chamada [**Speak**](speak-method.md) ou [**Think**](think-method.md) com uma instrução para tentar alterar a propriedade do balão, ela não poderá afetar o estado visível do balão, pois a chamada **Speak** ou **Think** será enfileirada, mas a chamada definindo o estado visível do balão não.</span><span class="sxs-lookup"><span data-stu-id="98006-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="98006-117">Portanto, defina esse valor somente quando nenhuma chamada de **fala** ou **Think** estiver na fila do caractere.</span><span class="sxs-lookup"><span data-stu-id="98006-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="98006-118">Se você tentar definir essa propriedade enquanto o caractere estiver falando, movendo ou sendo arrastado, a configuração de propriedade não entrará em vigor até que a operação anterior seja concluída.</span><span class="sxs-lookup"><span data-stu-id="98006-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="98006-119">Chamar os métodos [**Speak**](speak-method.md) e [**Think**](think-method.md) automaticamente torna o balão visível, definindo a propriedade [**Visible**](visible-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="98006-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="98006-120">Se a propriedade AutoOcultar do balão do caractere estiver habilitada, o balão será ocultado automaticamente depois que o texto de saída for falado.</span><span class="sxs-lookup"><span data-stu-id="98006-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="98006-121">Clicar ou arrastar um caractere que não esteja falando no momento também ocultará automaticamente o balão mesmo se sua configuração de AutoOcultar estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="98006-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="98006-122">Você pode alterar a configuração de AutoOcultar do caractere usando a propriedade [**Style**](style-property.md) do balão.</span><span class="sxs-lookup"><span data-stu-id="98006-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="98006-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="98006-123">See Also</span></span>

[<span data-ttu-id="98006-124">**Propriedade de estilo**</span><span class="sxs-lookup"><span data-stu-id="98006-124">**Style property**</span></span>](style-property.md)


 

 





