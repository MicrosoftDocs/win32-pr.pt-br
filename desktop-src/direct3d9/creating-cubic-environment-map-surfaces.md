---
description: Você cria uma textura de mapa de ambiente cúbico chamando o método CreateCubeTexture. As texturas do mapa do ambiente cúbico devem ser quadradas, com dimensões que são uma potência de dois.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Criando superfícies de mapa de ambiente cúbico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36be3067c6a5f21c39cfed7cab731ca875b70799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500996"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a><span data-ttu-id="9db81-104">Criando superfícies de mapa de ambiente cúbico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9db81-104">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="9db81-105">Você cria uma textura de mapa de ambiente cúbico chamando o método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .</span><span class="sxs-lookup"><span data-stu-id="9db81-105">You create a cubic environment map texture by calling the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method.</span></span> <span data-ttu-id="9db81-106">As texturas do mapa do ambiente cúbico devem ser quadradas, com dimensões que são uma potência de dois.</span><span class="sxs-lookup"><span data-stu-id="9db81-106">Cubic environment map textures must be square, with dimensions that are a power of two.</span></span>

<span data-ttu-id="9db81-107">O exemplo de código a seguir mostra como seu aplicativo C++ pode criar um mapa de ambiente cúbico simples.</span><span class="sxs-lookup"><span data-stu-id="9db81-107">The following code example shows how your C++ application might create a simple cubic environment map.</span></span>


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a><span data-ttu-id="9db81-108">Acessando rostos de mapa de ambiente cúbico</span><span class="sxs-lookup"><span data-stu-id="9db81-108">Accessing Cubic Environment Map Faces</span></span>

<span data-ttu-id="9db81-109">Você pode navegar entre faces de um mapa de ambiente cúbico usando o método [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .</span><span class="sxs-lookup"><span data-stu-id="9db81-109">You can navigate between faces of a cubic environment map by using the [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) method.</span></span>

<span data-ttu-id="9db81-110">O exemplo de código a seguir usa [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) para recuperar a superfície do mapa de cubos usada para a face y positiva (face 2).</span><span class="sxs-lookup"><span data-stu-id="9db81-110">The following code example uses [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) to retrieve the cube-map surface used for the positive y-face (face 2).</span></span>


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



<span data-ttu-id="9db81-111">O primeiro parâmetro que o [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) aceita é um valor enumerado do [**\_ faces D3DCUBEMAP**](./d3dcubemap-faces.md) que descreve a superfície anexada que o método deve recuperar.</span><span class="sxs-lookup"><span data-stu-id="9db81-111">The first parameter that [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepts is a [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated value that describes the attached surface that the method should retrieve.</span></span> <span data-ttu-id="9db81-112">O segundo parâmetro informa ao Direct3D qual nível de uma textura de cubo mipmapped recuperar.</span><span class="sxs-lookup"><span data-stu-id="9db81-112">The second parameter tells Direct3D which level of a mipmapped cube texture to retrieve.</span></span> <span data-ttu-id="9db81-113">O terceiro parâmetro aceito é o endereço da interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , que representa a superfície de textura do cubo retornado.</span><span class="sxs-lookup"><span data-stu-id="9db81-113">The third parameter accepted is the address of the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the returned cube texture surface.</span></span> <span data-ttu-id="9db81-114">Como este mapa de cubos não é mipmapped, 0 é usado aqui.</span><span class="sxs-lookup"><span data-stu-id="9db81-114">Because this cube-map is not mipmapped, 0 is used here.</span></span>

> [!Note]
>
> <span data-ttu-id="9db81-115">Depois de chamar esse método, a contagem de referência interna na interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) é aumentada.</span><span class="sxs-lookup"><span data-stu-id="9db81-115">After calling this method, the internal reference count on the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface is increased.</span></span> <span data-ttu-id="9db81-116">Quando você terminar de usar essa superfície, não se esqueça de chamar o método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nessa interface **IDirect3DSurface9** ou terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="9db81-116">When you are done using this surface, be sure to call the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method on this **IDirect3DSurface9** interface or you will have a memory leak.</span></span>

 

## <a name="rendering-to-cubic-environment-maps"></a><span data-ttu-id="9db81-117">Renderizando para mapas de ambiente cúbico</span><span class="sxs-lookup"><span data-stu-id="9db81-117">Rendering to Cubic Environment Maps</span></span>

<span data-ttu-id="9db81-118">Você pode copiar imagens para as faces individuais do mapa do cubo, assim como faria com qualquer outro objeto de textura ou superfície.</span><span class="sxs-lookup"><span data-stu-id="9db81-118">You can copy images to the individual faces of the cube map just like you would any other texture or surface object.</span></span> <span data-ttu-id="9db81-119">A coisa mais importante a fazer antes de renderizar para uma face é definir as matrizes de transformação para que a câmera seja posicionada corretamente e aponte para a direção correta para essa face: encaminhar (+ z), voltar (-z), esquerda (-x), direita (+ x), up (+ y) ou Down (-y).</span><span class="sxs-lookup"><span data-stu-id="9db81-119">The most important thing to do before rendering to a face is set the transformation matrices so that the camera is positioned properly and points in the proper direction for that face: forward (+z), backward (-z), left (-x), right (+x), up (+y), or down (-y).</span></span>

<span data-ttu-id="9db81-120">O exemplo de código C++ a seguir prepara e define uma matriz de exibição de acordo com a face que está sendo renderizada.</span><span class="sxs-lookup"><span data-stu-id="9db81-120">The following C++ code example prepares and sets a view matrix according to the face being rendered.</span></span>


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



<span data-ttu-id="9db81-121">Lembre-se de que cada face de um mapa de ambiente cúbico representa um campo de exibição de 90 graus.</span><span class="sxs-lookup"><span data-stu-id="9db81-121">Remember, each face of a cubic environment map represents a 90-degree field of view.</span></span> <span data-ttu-id="9db81-122">A menos que seu aplicativo exija um campo diferente de ângulo de exibição-para efeitos especiais, por exemplo, tome cuidado para definir a matriz de projeção de forma adequada.</span><span class="sxs-lookup"><span data-stu-id="9db81-122">Unless your application requires a different field of view angle - for special effects, for example - take care to set the projection matrix accordingly.</span></span>

<span data-ttu-id="9db81-123">Este exemplo de código cria e define uma matriz de projeção para o caso mais comum.</span><span class="sxs-lookup"><span data-stu-id="9db81-123">This code example creates and sets a projection matrix for the most common case.</span></span>


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



<span data-ttu-id="9db81-124">Quando a câmera está em posição e o conjunto de matrizes de projeção, você pode renderizar a cena.</span><span class="sxs-lookup"><span data-stu-id="9db81-124">When the camera is in position and the projection matrix set, you can render the scene.</span></span> <span data-ttu-id="9db81-125">Cada objeto na cena deve ser posicionado como você normalmente os posiciona.</span><span class="sxs-lookup"><span data-stu-id="9db81-125">Each object in the scene should be positioned as you would normally position them.</span></span> <span data-ttu-id="9db81-126">O exemplo de código a seguir, fornecido para integridade, descreve essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="9db81-126">The following code example, provided for completeness, outlines this task.</span></span>


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



<span data-ttu-id="9db81-127">Observe a chamada para o método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="9db81-127">Note the call to the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="9db81-128">Ao renderizar para as faces do mapa do cubo, você deve atribuir a face como a superfície de destino de renderização atual.</span><span class="sxs-lookup"><span data-stu-id="9db81-128">When rendering to the cube map faces, you must assign the face as the current render-target surface.</span></span> <span data-ttu-id="9db81-129">Os aplicativos que usam buffers de profundidade podem criar explicitamente um buffer de profundidade para o destino de renderização ou reatribuir um buffer de profundidade existente à superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9db81-129">Applications that use depth buffers can explicitly create a depth-buffer for the render-target, or reassign an existing depth-buffer to the render-target surface.</span></span> <span data-ttu-id="9db81-130">O exemplo de código acima usa a última abordagem.</span><span class="sxs-lookup"><span data-stu-id="9db81-130">The code sample above uses the latter approach.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9db81-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9db81-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9db81-132">Mapeamento de ambiente cúbico</span><span class="sxs-lookup"><span data-stu-id="9db81-132">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
