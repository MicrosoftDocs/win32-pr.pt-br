---
title: Propriedade Visible (objeto Commands)
description: Saiba mais sobre a Propriedade Visível do objeto Commands, que determina se a legenda da coleção Commands aparece no menu pop-up do caractere.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396251"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="d7488-103">Propriedade Visible (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="d7488-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="d7488-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7488-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d7488-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7488-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d7488-106">Retorna ou define um valor que determina se a legenda da coleção [**Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="d7488-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="d7488-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="d7488-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="d7488-108">*agent\***. Characters(**"* CharacterID *"\*\*). Commands.Visible* \*  \[  =  *boolean*\]</span><span class="sxs-lookup"><span data-stu-id="d7488-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="d7488-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d7488-109">Part</span></span>      | <span data-ttu-id="d7488-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7488-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7488-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="d7488-111">*boolean*</span></span> | <span data-ttu-id="d7488-112">Uma expressão booliana que especifica se o [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="d7488-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="d7488-113">**True** A legenda é exibida.</span><span class="sxs-lookup"><span data-stu-id="d7488-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="d7488-114">**False** A legenda não é exibida.</span><span class="sxs-lookup"><span data-stu-id="d7488-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7488-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7488-115">Remarks</span></span>

<span data-ttu-id="d7488-116">Para que a legenda apareça no menu pop-up do caractere quando seu aplicativo não for o cliente de entrada ativa, essa propriedade deverá ser definida como **True** e a propriedade [**Legenda**](caption-property.md) definida para sua coleção comandos.</span><span class="sxs-lookup"><span data-stu-id="d7488-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="d7488-117">Além disso, essa propriedade deve ser definida como **True** para que os comandos em sua coleção apareçam no menu pop-up quando seu aplicativo estiver ativo de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7488-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

