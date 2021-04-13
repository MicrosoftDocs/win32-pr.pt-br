---
title: Menus de contexto
description: Menus de contexto
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Lojas online do Windows Media Player, menus de contexto
- lojas online, menus de contexto
- tipos 1 lojas online, menus de contexto
- Lojas online do Windows Media Player, menus de contexto personalizados
- lojas online, menus de contexto personalizados
- tipos 1 lojas online, menus de contexto personalizados
- menus de contexto
- menus de contexto personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365531"
---
# <a name="context-menus"></a><span data-ttu-id="71a89-111">Menus de contexto</span><span class="sxs-lookup"><span data-stu-id="71a89-111">Context Menus</span></span>

<span data-ttu-id="71a89-112">As lojas online podem fornecer menus de contexto personalizados.</span><span class="sxs-lookup"><span data-stu-id="71a89-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="71a89-113">Para fazer isso, o plug-in da loja online implementa o método [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) .</span><span class="sxs-lookup"><span data-stu-id="71a89-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="71a89-114">O Windows Media Player chama esse método para fornecer informações sobre o local na interface do usuário em que o menu de contexto é exibido (onde o usuário clicou com o botão direito do mouse).</span><span class="sxs-lookup"><span data-stu-id="71a89-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="71a89-115">O plug-in retorna uma matriz de estruturas [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que descrevem cada item de menu de contexto, incluindo uma ID de comando para cada.</span><span class="sxs-lookup"><span data-stu-id="71a89-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="71a89-116">Depois que o Windows Media Player tiver recuperado a matriz, o Player usará a matriz para criar o menu de contexto que o usuário vê.</span><span class="sxs-lookup"><span data-stu-id="71a89-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="71a89-117">Quando o usuário clica em um item no menu de contexto, o Player chama [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passando a ID de comando associada ao item de menu por meio do parâmetro *dwCommandID* .</span><span class="sxs-lookup"><span data-stu-id="71a89-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="71a89-118">O Player também passa um valor de local de biblioteca e uma matriz de IDs que representa os itens sobre os quais o menu foi invocado, como uma matriz de IDs de faixa.</span><span class="sxs-lookup"><span data-stu-id="71a89-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="71a89-119">Usando essas informações, o plug-in pode iniciar qualquer processo apropriado em resposta ao clique do mouse do usuário.</span><span class="sxs-lookup"><span data-stu-id="71a89-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71a89-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71a89-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71a89-121">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="71a89-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




