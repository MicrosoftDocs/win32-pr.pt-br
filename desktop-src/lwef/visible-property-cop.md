---
title: Propriedade Visible (objeto Command)
description: Propriedade Visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105811735"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="4426c-103">Propriedade Visible (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="4426c-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="4426c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4426c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4426c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="4426c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4426c-106">Retorna ou define se o [**comando**](/windows/desktop/lwef/the-command-object) está visível no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="4426c-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="4426c-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="4426c-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="4426c-108">\*Agente \***. Caracteres (**"\* characterid *"**). Comandos (**"* name \*" \* *).* \*  \[  =  *Booliano* visível\]</span><span class="sxs-lookup"><span data-stu-id="4426c-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="4426c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4426c-109">Part</span></span>      | <span data-ttu-id="4426c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4426c-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4426c-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="4426c-111">*boolean*</span></span> | <span data-ttu-id="4426c-112">Uma expressão booliana que especifica se a legenda do [**comando**](/windows/desktop/lwef/the-command-object)aparece no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="4426c-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="4426c-113">**True** (padrão) a legenda é exibida.</span><span class="sxs-lookup"><span data-stu-id="4426c-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="4426c-114">**Falso** A legenda não aparece.</span><span class="sxs-lookup"><span data-stu-id="4426c-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4426c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4426c-115">Remarks</span></span>

<span data-ttu-id="4426c-116">Defina essa propriedade como **false** quando desejar incluir entrada de voz para suas próprias interfaces sem que elas apareçam no menu pop-up para o caractere.</span><span class="sxs-lookup"><span data-stu-id="4426c-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="4426c-117">Se você definir a propriedade [**legenda**](caption-property.md) de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) como a cadeia de caracteres vazia (""), o texto da legenda não será exibido no menu pop-up (por exemplo, como uma linha em branco), independentemente da configuração da propriedade [**visível**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4426c-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="4426c-118">A configuração da propriedade [**Visible**](visible-property.md) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) pai de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) não afeta a configuração da propriedade **visível** do **comando**.</span><span class="sxs-lookup"><span data-stu-id="4426c-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

