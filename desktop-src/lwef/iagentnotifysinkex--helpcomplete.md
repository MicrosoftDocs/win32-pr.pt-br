---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007420"
---
# <a name="iagentnotifysinkexhelpcomplete"></a><span data-ttu-id="d1dbc-103">IAgentNotifySinkEx::HelpComplete</span><span class="sxs-lookup"><span data-stu-id="d1dbc-103">IAgentNotifySinkEx::HelpComplete</span></span>

<span data-ttu-id="d1dbc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1dbc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

<span data-ttu-id="d1dbc-105">Notifica um aplicativo cliente quando o usuário seleciona um comando ou caractere para concluir o modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-105">Notifies a client application when the user selects a command or character to complete Help mode.</span></span>

-   <span data-ttu-id="d1dbc-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d1dbc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="d1dbc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d1dbc-108">Identificador do caractere para o qual o modo de ajuda foi concluído.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-108">Identifier of the character for which Help mode completed.</span></span>

</dd> <dt>

<span data-ttu-id="d1dbc-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="d1dbc-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="d1dbc-110">Identificador do comando selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-110">Identifier of the command the user selected.</span></span>

</dd> <dt>

<span data-ttu-id="d1dbc-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="d1dbc-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="d1dbc-112">A causa do evento, que pode ser os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d1dbc-112">The cause for the event, which may be the following values:</span></span>



| <span data-ttu-id="d1dbc-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d1dbc-113">Value</span></span>                                                                         | <span data-ttu-id="d1dbc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1dbc-114">Description</span></span>                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1dbc-115">**const CSHELPCAUSE curto não assinado** **\_ comando = 1;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-115">**const unsigned short** **CSHELPCAUSE\_COMMAND = 1;**</span></span><br/>             | <span data-ttu-id="d1dbc-116">O usuário selecionou um comando fornecido pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-116">The user selected a command supplied by your application.</span></span>                            |
| <span data-ttu-id="d1dbc-117">**const CSHELPCAUSE curto não assinado** **\_ OTHERPROGRAM = 2;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-117">**const unsigned short** **CSHELPCAUSE\_OTHERPROGRAM = 2;**</span></span><br/>        | <span data-ttu-id="d1dbc-118">O usuário selecionou o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-118">The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span> |
| <span data-ttu-id="d1dbc-119">**const CSHELPCAUSE curto não assinado** **\_ OPENCOMMANDSWINDOW = 3;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-119">**const unsigned short** **CSHELPCAUSE\_OPENCOMMANDSWINDOW = 3;**</span></span><br/>  | <span data-ttu-id="d1dbc-120">O usuário selecionou o comando abrir comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-120">The user selected the Open Voice Commands command.</span></span>                                   |
| <span data-ttu-id="d1dbc-121">**const CSHELPCAUSE curto não assinado** **\_ CLOSECOMMANDSWINDOW = 4;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-121">**const unsigned short** **CSHELPCAUSE\_CLOSECOMMANDSWINDOW = 4;**</span></span><br/> | <span data-ttu-id="d1dbc-122">O usuário selecionou o comando fechar comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-122">The user selected the Close Voice Commands command.</span></span>                                  |
| <span data-ttu-id="d1dbc-123">**const CSHELPCAUSE curto não assinado** **\_ = 5;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-123">**const unsigned short** **CSHELPCAUSE\_SHOWCHARACTER = 5;**</span></span><br/>       | <span data-ttu-id="d1dbc-124">O usuário selecionou o comando Mostrar *caracterename* .</span><span class="sxs-lookup"><span data-stu-id="d1dbc-124">The user selected the Show *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="d1dbc-125">**const CSHELPCAUSE curto não assinado** **\_ HIDECHARACTER = 6;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-125">**const unsigned short** **CSHELPCAUSE\_HIDECHARACTER = 6;**</span></span><br/>       | <span data-ttu-id="d1dbc-126">O usuário selecionou o comando Ocultar *caracterename* .</span><span class="sxs-lookup"><span data-stu-id="d1dbc-126">The user selected the Hide *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="d1dbc-127">**const CSHELPCAUSE caracteres curto não assinado** **\_ = 7;**</span><span class="sxs-lookup"><span data-stu-id="d1dbc-127">**const unsigned short** **CSHELPCAUSE\_CHARACTER = 7;**</span></span><br/>           | <span data-ttu-id="d1dbc-128">O usuário selecionou (clicou) o caractere.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-128">The user selected (clicked) the character.</span></span>                                           |



 

</dd> </dl>

<span data-ttu-id="d1dbc-129">Normalmente, o modo de ajuda é concluído quando o usuário clica ou arrasta o caractere ou seleciona um comando no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-129">Typically Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="d1dbc-130">Clicar em outro caractere ou em outro lugar na tela não cancela o modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-130">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="d1dbc-131">O cliente que define o modo de ajuda para o caractere pode cancelar o modo de ajuda definindo [**IAgentCharacter:: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) como **false**.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-131">The client that set Help mode for the character can cancel Help mode by setting [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) to **False**.</span></span> <span data-ttu-id="d1dbc-132">(Isso não dispara o evento **IAgentNotifySinkEx:: HelpComplete** .)</span><span class="sxs-lookup"><span data-stu-id="d1dbc-132">(This does not trigger the **IAgentNotifySinkEx::HelpComplete** event.)</span></span>

<span data-ttu-id="d1dbc-133">Quando o usuário seleciona um comando no menu pop-up do caractere no modo de ajuda, o servidor remove o menu, chama a ajuda com a [**HelpContextId**](helpcontextid-property.md)especificada do comando e envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-133">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="d1dbc-134">O contexto é contextual (também conhecido como o que é isso?) A janela da ajuda é exibida no local do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-134">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="d1dbc-135">Se o usuário selecionar o comando por entrada de voz, a janela da ajuda será exibida sobre o caractere.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-135">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="d1dbc-136">Se o caractere estiver fora da tela, a janela será exibida na tela mais próxima da posição atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-136">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="d1dbc-137">Se o servidor retornar *dwCommandID* como uma cadeia de caracteres vazia (""), ele indicará que o usuário selecionou um comando fornecido pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-137">If the server returns *dwCommandID* as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="d1dbc-138">Esse evento é enviado somente para o aplicativo cliente que coloca o caractere no modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="d1dbc-138">This event is sent only to the client application that places the character into Help mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1dbc-139">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d1dbc-139">See Also</span></span>

<span data-ttu-id="d1dbc-140">[**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx:: setidentificaçãodocontextodaajuda**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="d1dbc-140">[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>


 

