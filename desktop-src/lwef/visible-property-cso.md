---
title: Propriedade Visible (objeto Commands)
description: Propriedade Visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369156"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="e253a-103">Propriedade Visible (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="e253a-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="e253a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e253a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e253a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="e253a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e253a-106">Retorna ou define um valor que determina se a legenda da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) é exibida no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="e253a-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="e253a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="e253a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="e253a-108">\*Agente \***. Caracteres (**"\* characterid \*" \* *). Comandos.* \*  \[  =  *booliano* visível\]</span><span class="sxs-lookup"><span data-stu-id="e253a-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="e253a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e253a-109">Part</span></span>      | <span data-ttu-id="e253a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e253a-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e253a-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="e253a-111">*boolean*</span></span> | <span data-ttu-id="e253a-112">Uma expressão booliana que especifica se o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) aparece no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="e253a-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="e253a-113">**Verdadeiro** A legenda é exibida.</span><span class="sxs-lookup"><span data-stu-id="e253a-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="e253a-114">**Falso** A legenda não aparece.</span><span class="sxs-lookup"><span data-stu-id="e253a-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e253a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e253a-115">Remarks</span></span>

<span data-ttu-id="e253a-116">Para que a legenda apareça no menu pop-up do caractere quando seu aplicativo não for o cliente de entrada-ativo, essa propriedade deverá ser definida como **true** e a propriedade [**Caption**](caption-property.md) definida para a coleção de comandos.</span><span class="sxs-lookup"><span data-stu-id="e253a-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="e253a-117">Além disso, essa propriedade deve ser definida como **true** para que os comandos em sua coleção sejam exibidos no menu pop-up quando seu aplicativo for Input-active.</span><span class="sxs-lookup"><span data-stu-id="e253a-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

