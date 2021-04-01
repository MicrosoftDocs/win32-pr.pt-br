---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084472"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="67fb6-103">IAgentCharacterEx::SetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="67fb6-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="67fb6-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67fb6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="67fb6-105">Define o modo de ajuda contextual para o caractere.</span><span class="sxs-lookup"><span data-stu-id="67fb6-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="67fb6-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="67fb6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="67fb6-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="67fb6-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="67fb6-108">Sinalizador de modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="67fb6-108">Help mode flag.</span></span> <span data-ttu-id="67fb6-109">Se esse parâmetro for **true**, o Microsoft Agent ativará o modo de ajuda para o caractere.</span><span class="sxs-lookup"><span data-stu-id="67fb6-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="67fb6-110">Quando você define essa propriedade como **true**, o ponteiro do mouse muda para a imagem de ajuda contextual quando movido sobre o caractere ou sobre o menu pop-up para o caractere.</span><span class="sxs-lookup"><span data-stu-id="67fb6-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="67fb6-111">Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md) e sai do modo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="67fb6-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="67fb6-112">No modo de ajuda, o servidor não envia os eventos de [**clique**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)e [**Command**](command-event.md) , a menos que a propriedade [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="67fb6-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="67fb6-113">Nesse caso, o servidor enviará o evento de **clique** (não sai do modo de ajuda), mas apenas para o botão direito do mouse, para que você possa exibir o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="67fb6-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="67fb6-114">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="67fb6-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="67fb6-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="67fb6-115">See Also</span></span>

<span data-ttu-id="67fb6-116">[**IAgentCharacterEx:: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="67fb6-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 