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
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Criando superfícies de mapa de ambiente cúbico (Direct3D 9)

Você cria uma textura de mapa de ambiente cúbico chamando o método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) . As texturas do mapa do ambiente cúbico devem ser quadradas, com dimensões que são uma potência de dois.

O exemplo de código a seguir mostra como seu aplicativo C++ pode criar um mapa de ambiente cúbico simples.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Acessando rostos de mapa de ambiente cúbico

Você pode navegar entre faces de um mapa de ambiente cúbico usando o método [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .

O exemplo de código a seguir usa [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) para recuperar a superfície do mapa de cubos usada para a face y positiva (face 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



O primeiro parâmetro que o [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) aceita é um valor enumerado do [**\_ faces D3DCUBEMAP**](./d3dcubemap-faces.md) que descreve a superfície anexada que o método deve recuperar. O segundo parâmetro informa ao Direct3D qual nível de uma textura de cubo mipmapped recuperar. O terceiro parâmetro aceito é o endereço da interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , que representa a superfície de textura do cubo retornado. Como este mapa de cubos não é mipmapped, 0 é usado aqui.

> [!Note]
>
> Depois de chamar esse método, a contagem de referência interna na interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) é aumentada. Quando você terminar de usar essa superfície, não se esqueça de chamar o método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nessa interface **IDirect3DSurface9** ou terá um vazamento de memória.

 

## <a name="rendering-to-cubic-environment-maps"></a>Renderizando para mapas de ambiente cúbico

Você pode copiar imagens para as faces individuais do mapa do cubo, assim como faria com qualquer outro objeto de textura ou superfície. A coisa mais importante a fazer antes de renderizar para uma face é definir as matrizes de transformação para que a câmera seja posicionada corretamente e aponte para a direção correta para essa face: encaminhar (+ z), voltar (-z), esquerda (-x), direita (+ x), up (+ y) ou Down (-y).

O exemplo de código C++ a seguir prepara e define uma matriz de exibição de acordo com a face que está sendo renderizada.


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



Lembre-se de que cada face de um mapa de ambiente cúbico representa um campo de exibição de 90 graus. A menos que seu aplicativo exija um campo diferente de ângulo de exibição-para efeitos especiais, por exemplo, tome cuidado para definir a matriz de projeção de forma adequada.

Este exemplo de código cria e define uma matriz de projeção para o caso mais comum.


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



Quando a câmera está em posição e o conjunto de matrizes de projeção, você pode renderizar a cena. Cada objeto na cena deve ser posicionado como você normalmente os posiciona. O exemplo de código a seguir, fornecido para integridade, descreve essa tarefa.


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



Observe a chamada para o método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . Ao renderizar para as faces do mapa do cubo, você deve atribuir a face como a superfície de destino de renderização atual. Os aplicativos que usam buffers de profundidade podem criar explicitamente um buffer de profundidade para o destino de renderização ou reatribuir um buffer de profundidade existente à superfície de destino de renderização. O exemplo de código acima usa a última abordagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de ambiente cúbico](cubic-environment-mapping.md)
</dt> </dl>

 

 
