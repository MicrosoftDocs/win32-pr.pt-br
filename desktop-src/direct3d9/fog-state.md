---
description: Os efeitos de neblina podem dar uma cena 3D maior realm.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Estado de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370035"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="32fce-103">Estado de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="32fce-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="32fce-104">Os efeitos de neblina podem dar uma cena 3D maior realm.</span><span class="sxs-lookup"><span data-stu-id="32fce-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="32fce-105">Você pode usar efeitos de neblina para mais do que simular a neblina.</span><span class="sxs-lookup"><span data-stu-id="32fce-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="32fce-106">Eles também podem diminuir a clareza de uma cena com distância.</span><span class="sxs-lookup"><span data-stu-id="32fce-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="32fce-107">Isso espelha o que acontece no mundo real; à medida que os objetos se tornam mais distantes do usuário, seus detalhes são menos distintos.</span><span class="sxs-lookup"><span data-stu-id="32fce-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="32fce-108">Para obter mais informações sobre como usar a neblina em seu aplicativo, consulte [neblina (Direct3D 9)](fog.md).</span><span class="sxs-lookup"><span data-stu-id="32fce-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="32fce-109">Um aplicativo C++ controla a neblina por meio de Estados de renderização de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32fce-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="32fce-110">O tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) inclui Estados para controlar se pixel (tabela) ou sombra de vértice é usado, qual cor é, a fórmula de neblina que o sistema aplica e os parâmetros da fórmula.</span><span class="sxs-lookup"><span data-stu-id="32fce-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="32fce-111">Você habilita a neblina definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGENABLE como **true**.</span><span class="sxs-lookup"><span data-stu-id="32fce-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="32fce-112">A cor de neblina pode ser definida como qualquer valor de cor usando o \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR; o componente alfa da cor de neblina é ignorado.</span><span class="sxs-lookup"><span data-stu-id="32fce-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="32fce-113">Os \_ Estados de RENDERIZAÇÃO D3DRS FOGTABLEMODE e D3DRS \_ FOGVERTEXMODE controlam a fórmula de neblina aplicada para cálculos de neblina e controlam indiretamente qual tipo de neblina é aplicado.</span><span class="sxs-lookup"><span data-stu-id="32fce-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="32fce-114">Ambos os Estados de processamento podem ser definidos como um membro do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="32fce-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="32fce-115">A configuração de Process State como D3DFOG \_ None desabilita a sombra de pixel ou Vertex, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="32fce-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="32fce-116">Se ambos os Estados de renderização estiverem definidos como modos válidos, o sistema aplicará apenas efeitos de neblina de pixel.</span><span class="sxs-lookup"><span data-stu-id="32fce-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="32fce-117">Os Estados de renderização de D3DRS \_ FOGSTART e D3DRS \_ FOGEND do controle de parâmetros de fórmulas de neblina para o modo de D3DFOG \_ linear.</span><span class="sxs-lookup"><span data-stu-id="32fce-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="32fce-118">Os controles de estado de renderização de D3DRS FOGDENSITY são uma \_ densidade de neblina nos modos de neblina exponencial.</span><span class="sxs-lookup"><span data-stu-id="32fce-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="32fce-119">Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="32fce-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32fce-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32fce-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32fce-121">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="32fce-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
