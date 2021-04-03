---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916394"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="78601-103">Evento DeactivateInput</span><span class="sxs-lookup"><span data-stu-id="78601-103">DeactivateInput Event</span></span>

<span data-ttu-id="78601-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="78601-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="78601-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="78601-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="78601-106">Ocorre quando um cliente se torna não-entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="78601-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="78601-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="78601-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="78601-108">**Sub** *Agent \* \* \* \_ DeactivateInput* \*  **(ByVal** *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="78601-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="78601-109">Parte</span><span class="sxs-lookup"><span data-stu-id="78601-109">Part</span></span>          | <span data-ttu-id="78601-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="78601-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="78601-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="78601-111">*CharacterID*</span></span> | <span data-ttu-id="78601-112">Retorna a ID do caractere que faz com que o cliente se torne não-entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="78601-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="78601-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="78601-113">Remarks</span></span>

<span data-ttu-id="78601-114">Um cliente de não entrada-ativo não recebe mais eventos de mouse ou fala do servidor (a menos que ele se torne de entrada-ativo novamente).</span><span class="sxs-lookup"><span data-stu-id="78601-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="78601-115">O servidor envia esse evento somente para o cliente que se torna não-ativo.</span><span class="sxs-lookup"><span data-stu-id="78601-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="78601-116">Esse evento ocorre quando o aplicativo cliente é de entrada-ativo e o usuário escolhe a legenda de outro cliente no menu pop-up de um caractere ou na janela comandos de voz ou você chama o método [**Activate**](activate-method.md) e define o parâmetro **State** como 0.</span><span class="sxs-lookup"><span data-stu-id="78601-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="78601-117">Isso também pode ocorrer quando o usuário seleciona o nome de outro caractere clicando ou falando.</span><span class="sxs-lookup"><span data-stu-id="78601-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="78601-118">Você também receberá esse evento quando seu caractere estiver oculto ou se outro caractere ficar visível.</span><span class="sxs-lookup"><span data-stu-id="78601-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="78601-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="78601-119">See Also</span></span>

[<span data-ttu-id="78601-120">**Evento ActivateInput**</span><span class="sxs-lookup"><span data-stu-id="78601-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




