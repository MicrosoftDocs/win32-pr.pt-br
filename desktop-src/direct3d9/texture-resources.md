---
description: Os recursos de textura são implementados na interface IDirect3DTexture9. Para obter um ponteiro para uma interface de textura, chame o método IDirect3DDevice9::CreateTexture ou qualquer uma das funções D3DX a seguir.
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Recursos de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230caaa352a50644a6580c8aae28f18882425e40d9378cbafee1980cf317aa46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290684"
---
# <a name="texture-resources-direct3d-9"></a>Recursos de textura (Direct3D 9)

Os recursos de textura são implementados na interface [**IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) Para obter um ponteiro para uma interface de textura, chame o método [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) ou qualquer uma das funções D3DX a seguir.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

O exemplo de código a seguir [**usa D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) para carregar uma textura de Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



O primeiro parâmetro aceito [**por D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) é um ponteiro para uma interface [**IDirect3DDevice9.**](/windows/desktop/api) O segundo parâmetro informa ao Direct3D o nome do arquivo do qual carregar a textura. O terceiro parâmetro leva o endereço de um ponteiro para uma interface [**IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa o objeto de textura criado.

## <a name="rendering-with-texture-resources"></a>Renderização com recursos de textura

O Direct3D dá suporte à mesclagem de várias texturas pelo conceito de estágios de textura. Cada estágio de textura contém uma textura e as operações que podem ser executadas na textura. As texturas nos estágios de textura formam o conjunto de texturas atuais. Para obter mais informações, consulte [Blending de textura (Direct3D 9)](texture-blending.md). O estado de cada textura é encapsulado em seu estágio de textura.

Em um aplicativo C++, o estado de cada textura deve ser definido com o [**método IDirect3DDevice9::SetTextureStageState.**](/windows/desktop/api) Passe o número do estágio (0-7) como o valor do primeiro parâmetro. De definir o valor do segundo parâmetro como um membro do tipo enumerado [**D3DTEXTURESTAGESTATETYPE.**](./d3dtexturestagestatetype.md) O parâmetro final é o valor de estado para o estado de textura específico.

Usando ponteiros de interface de textura, seu aplicativo pode renderizar uma combinação de até oito texturas. De definir as texturas atuais invocando o [**método IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) O Direct3D combina todas as texturas atuais nos primitivos que renderiza.

> [!Note]  
> O [**método IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa a contagem de referência da superfície de textura que está sendo atribuída. Quando a textura não for mais necessária, você deverá definir a textura no estágio apropriado como **NULL.** Se você não conseguir fazer isso, a superfície não será liberada, resultando em uma perda de memória.

 

Seu aplicativo pode definir o estado de quebra de textura para as texturas atuais chamando o [**método IDirect3DDevice9::SetRenderState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) Passe um valor de D3DRS WRAP0 para D3DRS WRAP7 como o valor do primeiro parâmetro e use uma combinação dos sinalizadores \_ \_ D3DWRAPCOORD \_ 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD 2 e \_ D3DWRAPCOORD \_ 3 para habilitar a quebra nas instruções u, v ou w.

Seu aplicativo também pode definir a perspectiva da textura e os estados de filtragem de textura. Consulte [Filtragem de textura (Direct3D 9)](texture-filtering.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
