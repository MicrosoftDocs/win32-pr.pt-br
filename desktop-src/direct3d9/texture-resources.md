---
description: 'Os recursos de textura são implementados na interface IDirect3DTexture9. Para obter um ponteiro para uma interface de textura, chame o método IDirect3DDevice9:: CreateTexture ou qualquer uma das funções D3DX a seguir.'
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Recursos de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163852"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="e8dbe-104">Recursos de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e8dbe-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="e8dbe-105">Os recursos de textura são implementados na interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="e8dbe-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="e8dbe-106">Para obter um ponteiro para uma interface de textura, chame o método [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) ou qualquer uma das funções D3DX a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="e8dbe-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="e8dbe-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="e8dbe-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="e8dbe-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="e8dbe-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="e8dbe-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="e8dbe-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="e8dbe-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="e8dbe-114">O exemplo de código a seguir usa [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) para carregar uma textura de Tiger.bmp.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="e8dbe-115">O primeiro parâmetro que o [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) aceita é um ponteiro para uma interface [**IDirect3DDevice9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e8dbe-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="e8dbe-116">O segundo parâmetro informa ao Direct3D o nome do arquivo do qual carregar a textura.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="e8dbe-117">O terceiro parâmetro pega o endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="e8dbe-118">Renderizando com recursos de textura</span><span class="sxs-lookup"><span data-stu-id="e8dbe-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="e8dbe-119">O Direct3D dá suporte à mesclagem de várias texturas pelo conceito de estágios de textura.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="e8dbe-120">Cada estágio de textura contém uma textura e as operações que podem ser executadas na textura.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="e8dbe-121">As texturas nos estágios de textura formam o conjunto de texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="e8dbe-122">Para obter mais informações, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbe-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="e8dbe-123">O estado de cada textura é encapsulado em seu estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="e8dbe-124">Em um aplicativo C++, o estado de cada textura deve ser definido com o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e8dbe-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e8dbe-125">Passe o número do estágio (0-7) como o valor do primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="e8dbe-126">Defina o valor do segundo parâmetro como um membro do tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="e8dbe-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="e8dbe-127">O parâmetro final é o valor de estado para o estado de textura específico.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="e8dbe-128">Usando ponteiros de interface de textura, seu aplicativo pode renderizar uma mistura de até oito texturas.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="e8dbe-129">Defina as texturas atuais invocando o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="e8dbe-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="e8dbe-130">O Direct3D combina todas as texturas atuais para os primitivos que ele renderiza.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="e8dbe-131">O método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa a contagem de referência da superfície de textura que está sendo atribuída.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="e8dbe-132">Quando a textura não for mais necessária, você deverá definir a textura no estágio apropriado como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="e8dbe-133">Se você não conseguir fazer isso, a superfície não será liberada, resultando em um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="e8dbe-134">Seu aplicativo pode definir o estado de disposição da textura para as texturas atuais chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) .</span><span class="sxs-lookup"><span data-stu-id="e8dbe-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="e8dbe-135">Passe um valor de D3DRS \_ WRAP0 até D3DRS \_ WRAP7 como o valor do primeiro parâmetro e use uma combinação dos \_ sinalizadores D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 e D3DWRAPCOORD \_ 3 para habilitar o encapsulamento nas direções u, v ou w.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="e8dbe-136">Seu aplicativo também pode definir a perspectiva da textura e os estados de filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="e8dbe-137">Consulte [filtragem de textura (Direct3D 9)](texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbe-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8dbe-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8dbe-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8dbe-139">Texturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e8dbe-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
