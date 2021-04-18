---
description: Para criar um dispositivo Direct3D, primeiro crie um objeto Direct3D (consulte Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Criando um dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793933"
---
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="1c1b2-103">Criando um dispositivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1c1b2-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="1c1b2-104">Para criar um dispositivo Direct3D, primeiro crie um objeto Direct3D (consulte [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span><span class="sxs-lookup"><span data-stu-id="1c1b2-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="1c1b2-105">Todos os dispositivos de renderização criados por um objeto do Direct3D compartilham os mesmos recursos físicos.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="1c1b2-106">Se você criar vários dispositivos de renderização a partir de um único objeto do Direct3D, as penalidades de desempenho extremo serão incorridas porque compartilham o mesmo hardware.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="1c1b2-107">Primeiro, inicialize os valores para a estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) que é usada para criar o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="1c1b2-108">O exemplo de código a seguir especifica um aplicativo em janela onde o buffer de fundo é copiado para o buffer frontal durante uma operação de sincronização vertical somente.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="1c1b2-109">Em seguida, crie o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="1c1b2-110">A chamada [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) a seguir especifica o adaptador padrão, um dispositivo HAL (camada de abstração de hardware) e processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="1c1b2-111">Observe que uma chamada para criar, liberar ou redefinir o dispositivo deve ocorrer somente no mesmo thread que o procedimento de janela da janela de foco.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="1c1b2-112">Depois de criar o dispositivo, defina seu estado.</span><span class="sxs-lookup"><span data-stu-id="1c1b2-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c1b2-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c1b2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c1b2-114">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="1c1b2-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
