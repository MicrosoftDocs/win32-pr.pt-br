---
description: Um buffer de profundidade é uma propriedade do dispositivo. Para criar um buffer de profundidade gerenciado pelo Direct3D, defina os membros apropriados da estrutura de parâmetros D3DPRESENT, \_ conforme mostrado no exemplo de código a seguir.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Criando um buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088991"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="6ad9d-104">Criando um buffer de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6ad9d-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="6ad9d-105">Um buffer de profundidade é uma propriedade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="6ad9d-106">Para criar um buffer de profundidade gerenciado pelo Direct3D, defina os membros apropriados da estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="6ad9d-107">Ao definir o membro EnableAutoDepthStencil como **true**, você instrui o Direct3D a gerenciar buffers de profundidade para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="6ad9d-108">Observe que AutoDepthStencilFormat deve ser definido como um formato de buffer de profundidade válido.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="6ad9d-109">O \_ sinalizador D3DFMT D16 especifica um buffer de profundidade de 16 bits, se houver um disponível.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="6ad9d-110">A seguinte chamada para o método [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) cria um dispositivo que cria um buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="6ad9d-111">O buffer de profundidade é definido automaticamente como o destino de renderização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="6ad9d-112">Quando o dispositivo é redefinido, o buffer de profundidade é automaticamente destruído e recriado no novo tamanho.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="6ad9d-113">Para criar uma nova superfície de buffer de profundidade, use o método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="6ad9d-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="6ad9d-114">Para definir uma nova superfície de buffer de profundidade para o dispositivo, use o método [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="6ad9d-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="6ad9d-115">Para usar o buffer de profundidade em seu aplicativo, você precisa habilitar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6ad9d-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="6ad9d-116">Para obter detalhes, consulte [habilitando o buffer de profundidade (Direct3D 9)](enabling-depth-buffering.md).</span><span class="sxs-lookup"><span data-stu-id="6ad9d-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ad9d-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ad9d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ad9d-118">Buffers de profundidade</span><span class="sxs-lookup"><span data-stu-id="6ad9d-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
