---
title: Propriedade Visible (objeto Command)
description: Saiba mais sobre a Propriedade Visível do objeto Command, que retorna ou define se o Comando está visível no menu pop-up do caractere.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396241"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="8b3bd-103">Propriedade Visible (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="8b3bd-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="8b3bd-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b3bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8b3bd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8b3bd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8b3bd-106">Retorna ou define se [**o Comando**](/windows/desktop/lwef/the-command-object) está visível no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="8b3bd-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="8b3bd-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="8b3bd-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="8b3bd-108">*agent\***. Characters(**"* CharacterID *"**). Commands(**"* name *"\*\*). Booliana* \*  \[  =  *visível*\]</span><span class="sxs-lookup"><span data-stu-id="8b3bd-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="8b3bd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8b3bd-109">Part</span></span>      | <span data-ttu-id="8b3bd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b3bd-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3bd-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="8b3bd-111">*boolean*</span></span> | <span data-ttu-id="8b3bd-112">Uma expressão booliana que especifica se [**a**](/windows/desktop/lwef/the-command-object)legenda do Comando aparece no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="8b3bd-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="8b3bd-113">**True** (Padrão) A legenda é exibida.</span><span class="sxs-lookup"><span data-stu-id="8b3bd-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="8b3bd-114">**False** A legenda não é exibida.</span><span class="sxs-lookup"><span data-stu-id="8b3bd-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b3bd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b3bd-115">Remarks</span></span>

<span data-ttu-id="8b3bd-116">De definir essa propriedade como **False** quando você quiser incluir a entrada de voz para suas próprias interfaces sem que elas apareçam no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="8b3bd-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="8b3bd-117">Se você definir [**uma**](/windows/desktop/lwef/the-command-object) propriedade Legenda do objeto Command como a cadeia de caracteres vazia (""), o texto da legenda [](visible-property.md) não aparecerá no menu pop-up (por exemplo, como uma linha em branco), independentemente da configuração de propriedade Visible. [](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="8b3bd-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="8b3bd-118">A [**configuração**](visible-property.md) de propriedade Visible da [**coleção de**](/windows/desktop/lwef/the-command-object) Comandos pai de um objeto [**Command**](/windows/desktop/lwef/the-commands-collection-object) não afeta a **configuração de** propriedade Visible do **Comando**.</span><span class="sxs-lookup"><span data-stu-id="8b3bd-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

