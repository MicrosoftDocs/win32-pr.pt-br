---
description: Uma lista de alguns dos códigos de retorno possíveis para métodos e funções.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163759"
---
# <a name="s_present"></a><span data-ttu-id="e3620-103">S \_ presentes</span><span class="sxs-lookup"><span data-stu-id="e3620-103">S\_PRESENT</span></span>

<span data-ttu-id="e3620-104">Uma lista de alguns dos códigos de retorno possíveis para métodos e funções.</span><span class="sxs-lookup"><span data-stu-id="e3620-104">A list of some of the possible return codes for methods and functions.</span></span>



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3620-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="e3620-105">\#define</span></span>                  | <span data-ttu-id="e3620-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3620-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e3620-107">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="e3620-107">S\_OK</span></span>                     | <span data-ttu-id="e3620-108">O dispositivo está em execução normalmente e pode ser usado para renderização.</span><span class="sxs-lookup"><span data-stu-id="e3620-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e3620-109">\_obstruído presente \_ S</span><span class="sxs-lookup"><span data-stu-id="e3620-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="e3620-110">A área de apresentação é obstruído.</span><span class="sxs-lookup"><span data-stu-id="e3620-110">The presentation area is occluded.</span></span> <span data-ttu-id="e3620-111">Oclusão significa que a janela de apresentação está minimizada ou outro dispositivo entrou no modo de tela inteira no mesmo monitor que a janela de apresentação e a janela de apresentação está completamente no monitor.</span><span class="sxs-lookup"><span data-stu-id="e3620-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="e3620-112">Oclusão não ocorrerá se a área do cliente for coberta por outra janela.</span><span class="sxs-lookup"><span data-stu-id="e3620-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="e3620-113">Os aplicativos obstruído podem continuar a renderização e todas as chamadas terão sucesso, mas a janela de apresentação do obstruído não será atualizada.</span><span class="sxs-lookup"><span data-stu-id="e3620-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="e3620-114">Preferivelmente, o aplicativo deve parar de renderizar para a janela de apresentação usando o dispositivo e continuar chamando [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) até s \_ OK ou o modo de execução \_ \_ \_ alterado.</span><span class="sxs-lookup"><span data-stu-id="e3620-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="e3620-115">modo de S \_ atual \_ \_ alterado</span><span class="sxs-lookup"><span data-stu-id="e3620-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="e3620-116">O modo de exibição da área de trabalho foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e3620-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="e3620-117">O aplicativo pode continuar renderizando, mas pode haver conversão/alongamento de cores.</span><span class="sxs-lookup"><span data-stu-id="e3620-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="e3620-118">Escolha um formato de buffer de fundo semelhante ao modo de exibição atual e chame redefinir para recriar as cadeias de permuta.</span><span class="sxs-lookup"><span data-stu-id="e3620-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="e3620-119">O dispositivo deixará esse estado depois que uma redefinição for chamada.</span><span class="sxs-lookup"><span data-stu-id="e3620-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="e3620-120">Outros códigos de erro estão contidos em [D3DERR](d3derr.md).</span><span class="sxs-lookup"><span data-stu-id="e3620-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3620-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3620-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3620-122">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e3620-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




