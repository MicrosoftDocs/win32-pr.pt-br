---
title: A interface do usuário do Edge é suprimida nos cenários "in-out" e "inércia"
description: A interface do usuário do Edge é suprimida nos cenários "in-out" e "inércia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160369"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="bba90-103">A interface do usuário do Edge é suprimida nos cenários "in-out" e "inércia"</span><span class="sxs-lookup"><span data-stu-id="bba90-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="bba90-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="bba90-104">Platform</span></span>

<dl> <span data-ttu-id="bba90-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bba90-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="bba90-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bba90-106">Description</span></span>

<span data-ttu-id="bba90-107">Há alguns casos em que os usuários podem invocar involuntariamente a interface do usuário do Edge (botões, a barra de aplicativos e a troca de aplicativos).</span><span class="sxs-lookup"><span data-stu-id="bba90-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="bba90-108">Apresentamos um recurso para permitir que os desenvolvedores projetem sua interface do usuário para toda a tela sem fazer capacidades (por exemplo, bordas) para impedir que o usuário acesse acidentalmente as bordas.</span><span class="sxs-lookup"><span data-stu-id="bba90-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="bba90-109">Há dois casos que podem levar mais frequência a endedor de borda inadvertidamente:</span><span class="sxs-lookup"><span data-stu-id="bba90-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="bba90-110">No panorama rápido, a velocidade e a imprecisão da interação podem ocasionalmente fazer com que elas venham da borda da tela</span><span class="sxs-lookup"><span data-stu-id="bba90-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="bba90-111">Se os usuários saírem e reinserirem rapidamente a área da tela durante a criação de tinta com o dedo, por exemplo, em um aplicativo de pintura, esse comportamento de entrada pode acionar erroneamente a interface do usuário do Edge e interromper a experiência</span><span class="sxs-lookup"><span data-stu-id="bba90-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="bba90-112">Para melhorar a experiência do usuário e do desenvolvedor, a interface de usuário do Edge agora será suprimida em duas instâncias específicas:</span><span class="sxs-lookup"><span data-stu-id="bba90-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="bba90-113">Quando um usuário está panorâmica em um aplicativo que dá suporte a DManip inércia e passa para fora da tela enquanto o inércia está ocorrendo, a interface do usuário do Edge não será invocada dentro de uma janela de tempo limite</span><span class="sxs-lookup"><span data-stu-id="bba90-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="bba90-114">Em dispositivos certificados, quando um usuário passa rapidamente de dentro da tela para fora da tela e volta para dentro (movimento interno) dentro de determinados parâmetros, a interface do usuário do Edge não será invocada</span><span class="sxs-lookup"><span data-stu-id="bba90-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="bba90-115">Manifestações</span><span class="sxs-lookup"><span data-stu-id="bba90-115">Manifestations</span></span>

<span data-ttu-id="bba90-116">Os usuários que passarem rapidamente para a borda ao usar um aplicativo verão uma redução na invocação de borda não intencional.</span><span class="sxs-lookup"><span data-stu-id="bba90-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="bba90-117">Solução</span><span class="sxs-lookup"><span data-stu-id="bba90-117">Solution</span></span>

<span data-ttu-id="bba90-118">Os desenvolvedores devem manter essas atenuações em mente e devem ser capazes de usar a tela inteira sem medo de que os usuários dispararão acidentalmente a interface do usuário do Edge enquanto interagem com o aplicativo ao longo do limite.</span><span class="sxs-lookup"><span data-stu-id="bba90-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 




