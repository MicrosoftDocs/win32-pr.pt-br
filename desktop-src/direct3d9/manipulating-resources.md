---
description: Seu aplicativo manipula recursos para renderizar uma cena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipulando recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370033"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="4827a-103">Manipulando recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4827a-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="4827a-104">Seu aplicativo manipula recursos para renderizar uma cena.</span><span class="sxs-lookup"><span data-stu-id="4827a-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="4827a-105">Primeiro, um aplicativo precisa criar um recurso de textura com um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="4827a-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="4827a-106">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="4827a-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="4827a-107">**IDirect3DDevice9:: CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="4827a-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="4827a-108">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="4827a-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="4827a-109">Em vez disso, um recurso de textura pode ser criado com uma das funções D3DXCreatexxx texturing.</span><span class="sxs-lookup"><span data-stu-id="4827a-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="4827a-110">Os objetos de textura retornados pelos métodos de criação de textura são contêineres para superfícies ou volumes; esses contêineres são genericamente conhecidos como buffers.</span><span class="sxs-lookup"><span data-stu-id="4827a-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="4827a-111">Os buffers de Propriedade do recurso herdam os usos, o formato e o pool do recurso, mas têm seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="4827a-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="4827a-112">Para obter mais informações, consulte [Propriedades do recurso (Direct3D 9)](resource-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4827a-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="4827a-113">O aplicativo obtém acesso às superfícies contidas, com a finalidade de carregar o trabalho artístico, chamando os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4827a-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="4827a-114">Para obter detalhes, consulte [recursos de bloqueio (Direct3D 9)](locking-resources.md).</span><span class="sxs-lookup"><span data-stu-id="4827a-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="4827a-115">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="4827a-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="4827a-116">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="4827a-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="4827a-117">**IDirect3DVolumeTexture9:: LockBox**</span><span class="sxs-lookup"><span data-stu-id="4827a-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="4827a-118">Os métodos de bloqueio assumem argumentos que indicam a superfície contida, por exemplo, o subnível mipmap ou a face do cubo dos ponteiros de textura e de retorno para os pixels.</span><span class="sxs-lookup"><span data-stu-id="4827a-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="4827a-119">O aplicativo típico nunca usa um objeto Surface diretamente.</span><span class="sxs-lookup"><span data-stu-id="4827a-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="4827a-120">Crie recursos orientados a geometria chamando [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/desktop/api) ou [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span><span class="sxs-lookup"><span data-stu-id="4827a-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="4827a-121">Bloqueie e preencha os recursos de buffer chamando [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) ou [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), dependendo do recurso.</span><span class="sxs-lookup"><span data-stu-id="4827a-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="4827a-122">Para recursos de textura gerenciados, o processo de criação de recursos termina aqui.</span><span class="sxs-lookup"><span data-stu-id="4827a-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="4827a-123">Para recursos de textura não gerenciados, um aplicativo promove recursos de memória do sistema para recursos acessíveis ao dispositivo (para aceleração de hardware) chamando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="4827a-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="4827a-124">Para apresentar as imagens renderizadas a partir de recursos, o aplicativo também precisa de buffers de estêncil de profundidade e cor.</span><span class="sxs-lookup"><span data-stu-id="4827a-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="4827a-125">Para aplicativos típicos, o buffer de cores é de propriedade da cadeia de troca do dispositivo, que é uma coleção de superfícies de back-buffer e é criado implicitamente com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4827a-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="4827a-126">As superfícies de estêncil de profundidade podem ser criadas implicitamente ou explicitamente usando o método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="4827a-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="4827a-127">O aplicativo associa um dispositivo e seu buffer de profundidade e cor a uma chamada para [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) ou [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="4827a-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="4827a-128">Para obter detalhes sobre como apresentar a imagem final, consulte [apresentação de uma cena (Direct3D 9)](presenting-a-scene.md).</span><span class="sxs-lookup"><span data-stu-id="4827a-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4827a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4827a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4827a-130">Recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="4827a-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
