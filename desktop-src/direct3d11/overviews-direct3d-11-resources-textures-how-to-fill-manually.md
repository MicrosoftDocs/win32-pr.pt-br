---
title: Como inicializar uma textura programaticamente
description: Este tópico tem vários exemplos que mostram como inicializar texturas criadas com diferentes tipos de usos.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822772"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="5f411-103">Como: inicializar uma textura programaticamente</span><span class="sxs-lookup"><span data-stu-id="5f411-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="5f411-104">Você pode inicializar uma textura durante a criação do objeto ou pode preencher o objeto programaticamente após sua criação.</span><span class="sxs-lookup"><span data-stu-id="5f411-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="5f411-105">Este tópico tem vários exemplos que mostram como inicializar texturas criadas com diferentes tipos de usos.</span><span class="sxs-lookup"><span data-stu-id="5f411-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="5f411-106">Este exemplo pressupõe que você já sabe como [criar uma textura](overviews-direct3d-11-resources-textures-create.md).</span><span class="sxs-lookup"><span data-stu-id="5f411-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="5f411-107">Uso padrão</span><span class="sxs-lookup"><span data-stu-id="5f411-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="5f411-108">Uso dinâmico</span><span class="sxs-lookup"><span data-stu-id="5f411-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="5f411-109">Uso de preparo</span><span class="sxs-lookup"><span data-stu-id="5f411-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="5f411-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f411-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="5f411-111">Uso padrão</span><span class="sxs-lookup"><span data-stu-id="5f411-111">Default Usage</span></span>

<span data-ttu-id="5f411-112">O tipo de uso mais comum é o uso padrão.</span><span class="sxs-lookup"><span data-stu-id="5f411-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="5f411-113">Para preencher uma textura padrão (uma criada com **o \_ \_ padrão de uso D3D11**), você pode:</span><span class="sxs-lookup"><span data-stu-id="5f411-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="5f411-114">Chame [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inicialize *pInitialData* para apontar para os dados fornecidos de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f411-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="5f411-115">ou</span><span class="sxs-lookup"><span data-stu-id="5f411-115">or</span></span>

-   <span data-ttu-id="5f411-116">Depois de chamar [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para preencher a textura padrão com dados de um ponteiro fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f411-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="5f411-117">Uso dinâmico</span><span class="sxs-lookup"><span data-stu-id="5f411-117">Dynamic Usage</span></span>

<span data-ttu-id="5f411-118">Para preencher uma textura dinâmica (uma criada com **D3D11 \_ uso \_ dinâmico**):</span><span class="sxs-lookup"><span data-stu-id="5f411-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="5f411-119">Obtenha um ponteiro para a memória de textura passando no **D3D11 \_ map \_ Write \_ Discard** ao chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="5f411-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="5f411-120">Grave dados na memória.</span><span class="sxs-lookup"><span data-stu-id="5f411-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="5f411-121">Chame [**ID3D11DeviceContext:: Inmapear**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) quando terminar de gravar dados.</span><span class="sxs-lookup"><span data-stu-id="5f411-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="5f411-122">Uso de preparo</span><span class="sxs-lookup"><span data-stu-id="5f411-122">Staging Usage</span></span>

<span data-ttu-id="5f411-123">Para preencher uma textura de preparo (uma criada com **o \_ \_ preparo de uso do D3D11**):</span><span class="sxs-lookup"><span data-stu-id="5f411-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="5f411-124">Obtenha um ponteiro para a memória de textura passando a **\_ \_ gravação do mapa D3D11** ao chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="5f411-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="5f411-125">Grave dados na memória.</span><span class="sxs-lookup"><span data-stu-id="5f411-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="5f411-126">Chame [**ID3D11DeviceContext:: Inmapear**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) quando terminar de gravar dados.</span><span class="sxs-lookup"><span data-stu-id="5f411-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="5f411-127">Uma textura de preparo pode ser usada como o parâmetro de origem para [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ou [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) para preencher um recurso padrão ou dinâmico.</span><span class="sxs-lookup"><span data-stu-id="5f411-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f411-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f411-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f411-129">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5f411-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="5f411-130">Texturas</span><span class="sxs-lookup"><span data-stu-id="5f411-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




