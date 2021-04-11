---
description: Os recursos são as texturas e os buffers que são usados para renderizar uma cena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Recursos do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087598"
---
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="37ec1-103">Recursos do Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="37ec1-104">Os recursos são as texturas e os buffers que são usados para renderizar uma cena.</span><span class="sxs-lookup"><span data-stu-id="37ec1-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="37ec1-105">Os aplicativos precisam criar, carregar, copiar e usar recursos.</span><span class="sxs-lookup"><span data-stu-id="37ec1-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="37ec1-106">Esta seção fornece uma breve introdução aos recursos e às etapas e aos métodos usados por aplicativos ao trabalhar com recursos.</span><span class="sxs-lookup"><span data-stu-id="37ec1-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="37ec1-107">Todos os recursos, incluindo os recursos de geometria [**IDirect3DIndexBuffer9**](/windows/desktop/api) e [**IDirect3DVertexBuffer9**](/windows/desktop/api), herdam da interface [**IDirect3DResource9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="37ec1-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="37ec1-108">Os recursos de textura, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)e [**IDirect3DVolumeTexture9**](/windows/desktop/api), também herdam da interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .</span><span class="sxs-lookup"><span data-stu-id="37ec1-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="37ec1-109">Propriedades do recurso (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="37ec1-110">Manipulando recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="37ec1-111">Recursos de bloqueio (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="37ec1-112">Relações de recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="37ec1-113">Gerenciando recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="37ec1-114">Recursos gerenciados por aplicativo e estratégias de alocação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="37ec1-115">Buffers de índice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="37ec1-116">Buffers de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37ec1-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="37ec1-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37ec1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ec1-118">Introdução</span><span class="sxs-lookup"><span data-stu-id="37ec1-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
