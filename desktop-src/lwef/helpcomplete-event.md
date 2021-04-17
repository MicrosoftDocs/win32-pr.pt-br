---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105763818"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="a7370-103">Evento HelpComplete</span><span class="sxs-lookup"><span data-stu-id="a7370-103">HelpComplete Event</span></span>

<span data-ttu-id="a7370-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7370-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a7370-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="a7370-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a7370-106">Indica que o modo de ajuda contextual foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="a7370-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="a7370-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="a7370-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a7370-108">**Sub** *Agent. \* \* \* (ByVal* \*  \*characterid \* \* *, ByVal* \*  \*Name \* \* *, ByVal* \*  *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="a7370-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="a7370-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a7370-109">Part</span></span>          | <span data-ttu-id="a7370-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7370-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7370-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="a7370-111">*CharacterID*</span></span> | <span data-ttu-id="a7370-112">Retorna a ID do caractere clicado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a7370-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a7370-113">*Nome*</span><span class="sxs-lookup"><span data-stu-id="a7370-113">*Name*</span></span>        | <span data-ttu-id="a7370-114">Retorna um valor de cadeia de caracteres que identifica o nome (ID) do comando.</span><span class="sxs-lookup"><span data-stu-id="a7370-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a7370-115">*Causa*</span><span class="sxs-lookup"><span data-stu-id="a7370-115">*Cause*</span></span>       | <span data-ttu-id="a7370-116">Retorna um valor que indica o que causou a conclusão do modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="a7370-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="a7370-117">1 o usuário selecionou um comando fornecido pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7370-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="a7370-118">2 o usuário selecionou o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente.</span><span class="sxs-lookup"><span data-stu-id="a7370-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="a7370-119">3 o usuário selecionou o comando abrir comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="a7370-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="a7370-120">4 o usuário selecionou o comando fechar comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="a7370-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="a7370-121">5 o usuário selecionou o comando Mostrar *caracterename* .</span><span class="sxs-lookup"><span data-stu-id="a7370-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="a7370-122">6 o usuário selecionou o comando Ocultar *caracterename* .</span><span class="sxs-lookup"><span data-stu-id="a7370-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="a7370-123">7 o usuário selecionou (clicou) o caractere.</span><span class="sxs-lookup"><span data-stu-id="a7370-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="a7370-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7370-124">Remarks</span></span>

<span data-ttu-id="a7370-125">Normalmente, o modo de ajuda é concluído quando o usuário clica ou arrasta o caractere ou seleciona um comando no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="a7370-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="a7370-126">Clicar em outro caractere ou em outro lugar na tela não cancela o modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="a7370-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="a7370-127">O cliente que define o modo de ajuda para o caractere pode cancelar o modo de ajuda definindo [**HelpModeOn**](helpmodeon-property.md) como **false**.</span><span class="sxs-lookup"><span data-stu-id="a7370-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="a7370-128">(Isso não dispara o evento **HelpComplete** .)</span><span class="sxs-lookup"><span data-stu-id="a7370-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="a7370-129">Quando o usuário seleciona um comando no menu pop-up do caractere no modo de ajuda, o servidor remove o menu, chama a ajuda com a [**HelpContextId**](helpcontextid-property.md)especificada do comando e envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="a7370-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="a7370-130">O contexto é contextual (também conhecido como o que é isso?) A janela da ajuda é exibida no local do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a7370-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="a7370-131">Se o usuário selecionar o comando por entrada de voz, a janela da ajuda será exibida sobre o caractere.</span><span class="sxs-lookup"><span data-stu-id="a7370-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="a7370-132">Se o caractere estiver fora da tela, a janela será exibida na tela mais próxima da posição atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="a7370-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="a7370-133">Se o servidor retornar um nome como uma cadeia de caracteres vazia (""), ele indicará que o usuário selecionou um comando fornecido pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a7370-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="a7370-134">Esse evento é enviado somente para o aplicativo cliente que coloca o caractere no modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="a7370-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="a7370-135">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a7370-135">See Also</span></span>

<span data-ttu-id="a7370-136">[**Propriedade HelpModeOn**](helpmodeon-property.md), [ **propriedade HelpContextID**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="a7370-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

