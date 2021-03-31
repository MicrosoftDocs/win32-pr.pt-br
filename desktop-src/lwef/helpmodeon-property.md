---
title: Propriedade HelpModeOn
description: Propriedade HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636043"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="4e470-103">Propriedade HelpModeOn</span><span class="sxs-lookup"><span data-stu-id="4e470-103">HelpModeOn Property</span></span>

<span data-ttu-id="4e470-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e470-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4e470-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="4e470-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4e470-106">Retorna ou define se o modo de ajuda contextual está ativado para o caractere.</span><span class="sxs-lookup"><span data-stu-id="4e470-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="4e470-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="4e470-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4e470-108">\*agente do. ***Caracteres ("*** characterid \* \* *"). HelpModeOn* \*  \[  =  *booliano*\]</span><span class="sxs-lookup"><span data-stu-id="4e470-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="4e470-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4e470-109">Part</span></span>      | <span data-ttu-id="4e470-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e470-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e470-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="4e470-111">*boolean*</span></span> | <span data-ttu-id="4e470-112">Uma expressão booliana que especifica se o modo de ajuda contextual está ativado.</span><span class="sxs-lookup"><span data-stu-id="4e470-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="4e470-113">**Verdadeiro** O modo de ajuda está ativado.</span><span class="sxs-lookup"><span data-stu-id="4e470-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="4e470-114">**False** (padrão) o modo de ajuda é desativado.</span><span class="sxs-lookup"><span data-stu-id="4e470-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e470-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e470-115">Remarks</span></span>

<span data-ttu-id="4e470-116">Quando você define essa propriedade como **true**, o ponteiro do mouse muda para a imagem de ajuda contextual quando movido sobre o caractere ou sobre o menu pop-up para o caractere.</span><span class="sxs-lookup"><span data-stu-id="4e470-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="4e470-117">Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**HelpComplete**](helpcomplete-event.md) e sai do modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="4e470-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="4e470-118">No modo de ajuda, o servidor não envia os eventos de [**clique**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)e [**Command**](command-event.md) , a menos que você defina a propriedade [**AutoPopupMenu**](autopopupmenu-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="4e470-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="4e470-119">Nesse caso, o servidor enviará o evento de **clique** (não sai do modo de ajuda), mas apenas para o botão direito do mouse para permitir que você exiba o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="4e470-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="4e470-120">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4e470-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e470-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4e470-121">See Also</span></span>

[<span data-ttu-id="4e470-122">**Evento HelpComplete**</span><span class="sxs-lookup"><span data-stu-id="4e470-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





