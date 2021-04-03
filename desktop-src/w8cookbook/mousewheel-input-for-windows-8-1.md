---
title: Entrada MouseWheel para Windows 8.1
description: Entrada MouseWheel para Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822465"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="8abd5-103">Entrada MouseWheel para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8abd5-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="8abd5-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="8abd5-104">Platform</span></span>

<dl> <span data-ttu-id="8abd5-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8abd5-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="8abd5-106">Servidores-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8abd5-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="8abd5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8abd5-107">Description</span></span>

<span data-ttu-id="8abd5-108">Em Windows 8.1, os eventos MouseWheel não são mais entregues com base no foco do teclado como nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="8abd5-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="8abd5-109">Em Windows 8.1, se o mouse estiver focalizando um aplicativo da loja, o MouseWheel será entregue a esse aplicativo; para fins de compatibilidade, no entanto, se o mouse estiver focalizando um aplicativo de área de trabalho, o MouseWheel continuará a ser entregue com base no foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="8abd5-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="8abd5-110">Manifestações</span><span class="sxs-lookup"><span data-stu-id="8abd5-110">Manifestations</span></span>

<span data-ttu-id="8abd5-111">Quando o mouse estiver focalizando os aplicativos da loja, o MouseWheel rolará qualquer conteúdo aplicável sem que o usuário precise clicar no aplicativo da loja.</span><span class="sxs-lookup"><span data-stu-id="8abd5-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="8abd5-112">Isso também se aplica à tela inicial.</span><span class="sxs-lookup"><span data-stu-id="8abd5-112">This also applies to the start screen.</span></span> <span data-ttu-id="8abd5-113">Isso torna a rolagem por MouseWheel uma interação mais simples em Windows 8.1 do que no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8abd5-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8abd5-114">Atenuação</span><span class="sxs-lookup"><span data-stu-id="8abd5-114">Mitigation</span></span>

<span data-ttu-id="8abd5-115">Na maior parte, essa alteração não deve ter nenhum impacto sobre os aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="8abd5-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="8abd5-116">Se um aplicativo da loja tiver escutado por eventos MouseWheel somente depois de ter registrado um evento de clique do mouse, esse aplicativo não provavelmente responderia ao MouseWheel até que o usuário o tenha clicado ativamente.</span><span class="sxs-lookup"><span data-stu-id="8abd5-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="8abd5-117">Consequentemente, a desvantagem mais provável aqui é simplesmente que um aplicativo continua a operar da mesma forma que no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8abd5-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="8abd5-118">Para aplicativos da área de trabalho, o foco do teclado não dá mais ao aplicativo uma monopolização da entrada MouseWheel, mas isso também não faz nenhum tipo de quebra desses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8abd5-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="8abd5-119">Portanto, nenhuma mitigação de curto prazo é necessária.</span><span class="sxs-lookup"><span data-stu-id="8abd5-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="8abd5-120">Solução</span><span class="sxs-lookup"><span data-stu-id="8abd5-120">Solution</span></span>

<span data-ttu-id="8abd5-121">Os desenvolvedores de aplicativos da loja devem esperar receber eventos MouseWheel sem um evento de clique do mouse com o cursor.</span><span class="sxs-lookup"><span data-stu-id="8abd5-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="8abd5-122">Eles não devem, por exemplo, escutar eventos MouseWheel somente depois de registrar um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="8abd5-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="8abd5-123">Da mesma forma, os aplicativos de área de trabalho não devem tentar capturar eventos MouseWheel (por exemplo, definindo um gancho de nível baixo) quando têm o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="8abd5-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="8abd5-124">Testes</span><span class="sxs-lookup"><span data-stu-id="8abd5-124">Tests</span></span>

<span data-ttu-id="8abd5-125">Os desenvolvedores de aplicativos da loja devem testar Windows 8.1 para verificar se toda a funcionalidade de rolagem funciona sempre que o mouse está focalizando o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8abd5-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="8abd5-126">Os desenvolvedores de aplicativos de desktop devem testar Windows 8.1 para verificar se eles não estão capturando eventos MouseWheel (segundo diretrizes acima).</span><span class="sxs-lookup"><span data-stu-id="8abd5-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 




