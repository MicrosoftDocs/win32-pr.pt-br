---
description: Usando texturas compactadas (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Usando texturas compactadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646175"
---
# <a name="using-compressed-textures-direct3d-9"></a>Usando texturas compactadas (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Determinando o suporte para texturas compactadas

Para testar o adaptador, especifique qualquer formato de pixel que use DXT1, DXT2, DXT3, DXT4 ou DXT5. Se [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) retornar o D3D \_ OK, o dispositivo poderá criar textura diretamente de uma superfície de textura compactada que usa esse formato. Nesse caso, você pode usar superfícies de textura compactadas diretamente com o Direct3D chamando o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . O exemplo de código a seguir mostra como determinar se o adaptador dá suporte a um formato de textura compactada.


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



Se o dispositivo não oferecer suporte a texturing de superfícies de textura compactadas, você ainda poderá armazenar dados de textura em uma superfície de formato compactado, mas deverá converter quaisquer texturas compactadas em um formato com suporte antes que possam ser usadas para texturing.

## <a name="creating-compressed-textures"></a>Criando texturas compactadas

Depois de criar um dispositivo que dá suporte a um formato de textura compactada no adaptador, você pode criar um recurso de textura compactada. Chame [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e especifique um formato de textura compactada para o parâmetro format.

Antes de carregar uma imagem em um objeto de textura, recupere um ponteiro para a superfície de textura chamando o método [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .

Agora você pode usar qualquer função D3DXLoadSurfacexxx para carregar uma imagem na superfície que foi recuperada usando [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel). Essas funções manipulam a conversão de e para formatos de textura compactados.

Você pode criar e converter arquivos de textura compactada (DDS) usando o editor de textura DirectX (Dxtex.exe) fornecido com o SDK do DirectX. Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

A vantagem desse comportamento é que um aplicativo pode copiar o conteúdo de uma superfície compactada para um arquivo sem calcular a quantidade de armazenamento necessária para uma superfície de uma largura e altura específicas no formato específico.

A tabela a seguir mostra os cinco tipos de texturas compactadas. Para obter mais informações sobre como os dados são armazenados, consulte [formatos de textura compactados (Direct3D 9)](compressed-texture-formats.md). Você só precisará dessas informações se estiver escrevendo suas próprias rotinas de compactação.



| FOURCC | Descrição        | Alfa precalculado? |
|--------|--------------------|----------------------|
| DXT1   | Opaco/1 bit alfa | N/D                  |
| DXT2   | Alfa explícito     | Sim                  |
| DXT3   | Alfa explícito     | Não                   |
| DXT4   | Alfa interpolado | Sim                  |
| DXT5   | Alfa interpolado | Não                   |



 

Quando você transfere dados de um formato nonpremultiplied para um formato premultiplicado, o Direct3D dimensiona as cores com base nos valores Alfa. Não há suporte para a transferência de dados de um formato premultiplicado para um formato nonpremultiplied. Se você tentar transferir dados de uma fonte alfa contramultiplicada para um destino alfa nonpremultiplied, o método retornará D3DERR \_ INVALIDCALL. Se você transferir dados de uma fonte alfa já multiplicada para um destino que não tem alfa, os componentes de cor de origem, que foram dimensionados por alfa, serão copiados como estão.

## <a name="decompressing-compressed-texture-surfaces"></a>Descompactando superfícies de textura compactadas

Assim como na compactação de uma superfície de textura, a descompactação de uma textura compactada é executada por meio de serviços de cópia de Direct3D.

Para copiar uma superfície de textura compactada para uma superfície de textura descompactada, use a função [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md). Essas funções manipulam a compactação de e para superfícies compactadas e descompactadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de textura compactados](compressed-texture-resources.md)
</dt> </dl>

 

 
