---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160323"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="d3193-103">IAgentCharacterEx::GetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="d3193-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="d3193-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d3193-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="d3193-105">Recupera se o modo de ajuda sensível ao contexto está ativado para o caractere.</span><span class="sxs-lookup"><span data-stu-id="d3193-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="d3193-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d3193-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d3193-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="d3193-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="d3193-108">Endereço de uma variável que recebe **true** se o modo de ajuda estiver ativado para o caractere e **false** se não.</span><span class="sxs-lookup"><span data-stu-id="d3193-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="d3193-109">Quando essa propriedade é definida como **true**, o ponteiro do mouse muda para a imagem de ajuda contextual quando movido sobre o caractere ou sobre o menu pop-up para o caractere.</span><span class="sxs-lookup"><span data-stu-id="d3193-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="d3193-110">Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**IAgentNotifySinkEx:: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) e sai do modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="d3193-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="d3193-111">No modo de ajuda, o servidor não envia os eventos [**IAgentNotifySink:: Click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D Ragcomplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , a menos que [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) Propriedade retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="d3193-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="d3193-112">Nesse caso, o servidor enviará o evento **IAgentNotifySink:: Click** (não sai do modo de ajuda), mas apenas para o botão direito do mouse para permitir que você exiba o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="d3193-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="d3193-113">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="d3193-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3193-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d3193-114">See Also</span></span>

[<span data-ttu-id="d3193-115">**IAgentCharacterEx::SetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="d3193-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 




