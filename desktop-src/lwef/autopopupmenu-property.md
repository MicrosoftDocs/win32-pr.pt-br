---
title: Propriedade AutoPopupMenu
description: Propriedade AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292572"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="22d48-103">Propriedade AutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="22d48-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="22d48-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22d48-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="22d48-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="22d48-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="22d48-106">Retorna ou define se clicar com o botão direito do mouse no caractere ou no ícone da barra de tarefas exibirá automaticamente o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="22d48-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="22d48-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="22d48-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="22d48-108">\*agente do. ***Caracteres \* \* \* \* ("*** characterid \* \* *"). AutoPopupMenu* \*  \[  =  *booliano*\]</span><span class="sxs-lookup"><span data-stu-id="22d48-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="22d48-109">Parte</span><span class="sxs-lookup"><span data-stu-id="22d48-109">Part</span></span>      | <span data-ttu-id="22d48-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="22d48-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d48-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="22d48-111">*boolean*</span></span> | <span data-ttu-id="22d48-112">Uma expressão booliana que especifica se o servidor exibe automaticamente o menu pop-up do caractere no clique com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="22d48-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="22d48-113">**True** (padrão) exibe o menu ao clicar com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="22d48-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="22d48-114">**Falso** Não exibe o menu ao clicar com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="22d48-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22d48-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="22d48-115">Remarks</span></span>

<span data-ttu-id="22d48-116">Ao definir essa propriedade como **false**, você pode criar seu próprio comportamento de manipulação de menus.</span><span class="sxs-lookup"><span data-stu-id="22d48-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="22d48-117">Para exibir o menu depois de definir essa propriedade como **false**, use o método [**ShowPopupMenu**](showpopupmenu-method.md) .</span><span class="sxs-lookup"><span data-stu-id="22d48-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="22d48-118">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="22d48-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="22d48-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="22d48-119">See Also</span></span>

[<span data-ttu-id="22d48-120">**Método ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="22d48-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 





