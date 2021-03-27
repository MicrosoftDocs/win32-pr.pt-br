---
description: O retângulo delimitador de todos os monitores é a tela virtual. A área de trabalho cobre a tela virtual em vez de um único monitor. A ilustração a seguir mostra uma possível disposição de três monitores.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: A tela virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989094"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="84d03-105">A tela virtual</span><span class="sxs-lookup"><span data-stu-id="84d03-105">The Virtual Screen</span></span>

<span data-ttu-id="84d03-106">O retângulo delimitador de todos os monitores é a *tela virtual*.</span><span class="sxs-lookup"><span data-stu-id="84d03-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="84d03-107">A área de trabalho cobre a tela virtual em vez de um único monitor.</span><span class="sxs-lookup"><span data-stu-id="84d03-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="84d03-108">A ilustração a seguir mostra uma possível disposição de três monitores.</span><span class="sxs-lookup"><span data-stu-id="84d03-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![ilustração mostrando três caixas que representam monitores organizados em uma caixa que representa a tela virtual](images/multimon-1.png)

<span data-ttu-id="84d03-110">O *monitor primário* contém a origem (0, 0).</span><span class="sxs-lookup"><span data-stu-id="84d03-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="84d03-111">Isso é para compatibilidade com aplicativos existentes que esperam um monitor com uma origem.</span><span class="sxs-lookup"><span data-stu-id="84d03-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="84d03-112">No entanto, o monitor primário não precisa estar no canto superior esquerdo da tela virtual.</span><span class="sxs-lookup"><span data-stu-id="84d03-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="84d03-113">Na Figura 1, é próximo do centro.</span><span class="sxs-lookup"><span data-stu-id="84d03-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="84d03-114">Quando o monitor primário não está no canto superior esquerdo da tela virtual, partes da tela virtual têm coordenadas negativas.</span><span class="sxs-lookup"><span data-stu-id="84d03-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="84d03-115">Como a organização dos monitores é definida pelo usuário, todos os aplicativos devem ser projetados para trabalhar com coordenadas negativas.</span><span class="sxs-lookup"><span data-stu-id="84d03-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="84d03-116">Para obter mais informações, consulte [várias considerações de monitor para programas mais antigos](multiple-monitor-considerations-for-older-programs.md).</span><span class="sxs-lookup"><span data-stu-id="84d03-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="84d03-117">As coordenadas da tela virtual são representadas por um valor de 16 bits assinado devido aos valores de 16 bits contidos em muitas mensagens existentes.</span><span class="sxs-lookup"><span data-stu-id="84d03-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="84d03-118">Assim, os limites da tela virtual são:</span><span class="sxs-lookup"><span data-stu-id="84d03-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



