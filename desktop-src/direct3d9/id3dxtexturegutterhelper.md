---
description: A interface ID3DXTextureGutterHelper é usada para criar e gerenciar regiões de medianiz em uma textura. As regiões da medianiz separam texturas e permitem a interpolação bilinear para evitar a renderização de artefatos em limites de textura.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interface ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298772"
---
# <a name="id3dxtexturegutterhelper-interface"></a>Interface ID3DXTextureGutterHelper

A interface ID3DXTextureGutterHelper é usada para criar e gerenciar regiões de medianiz em uma textura. As regiões da medianiz separam texturas e permitem a interpolação bilinear para evitar a renderização de artefatos em limites de textura.

O Get... os métodos fornecem acesso às estruturas de dados usadas pela aplicação... maneiras.

## <a name="members"></a>Membros

A interface **ID3DXTextureGutterHelper** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureGutterHelper** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXTextureGutterHelper** tem esses métodos.



| Método                                                                   | Descrição                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Aplica medianizes a um buffer de textura flutuante.<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | Aplica medianizes a um objeto de buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | Aplica medianizes a um objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | Recupera as coordenadas Texel barycentric.<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | Recupera o índice do tipo de malha ao qual cada Texel pertence.<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | Recebe um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | Recupera a altura da textura, em pixels.<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | Recupera as coordenadas de textura (u, v) de cada Texel.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Recupera a largura da textura, em pixels.<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | Reamostrar uma textura na parametrização desta gutterhelper.<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | Define as coordenadas Texel barycentric.<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | Define o índice do tipo de malha ao qual cada Texel pertence.<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | Define um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | Define as coordenadas de textura (u, v) de cada Texel.<br/>                                          |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Quando usado com PRT (transferência de radiante de computação), essa interface requer uma parametrização exclusiva do modelo. Cada Texel deve corresponder a um único ponto na superfície do modelo e vice-versa. Se o modelo incluir várias texturas, ele deverá ser dividido em partes separadas que contêm um objeto auxiliar de medianiz por textura.

 

Essa interface pode ser usada para gerar um mapa no espaço de textura no qual cada Texel está em uma das quatro classes.



| Classe Texel | Local Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ponto inválido; Texel não será usado.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triângulo interno.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Dentro da medianiz.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Na medianiz; Texel será avaliado como um exemplo completo nos métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

Para as classes 1 e 2, um Texel é armazenado com a face à qual ele pertence, juntamente com as coordenadas barycentric dos dois primeiros vértices dessa face. Os vértices da medianiz são atribuídos à borda mais próxima no espaço de textura.

Não há nenhuma classe de Texel 3.

A interface **ID3DXTextureGutterHelper** é obtida chamando a função [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .

O tipo LPD3DXTEXTUREGUTTERHELPER é definido como um ponteiro para a interface **ID3DXTextureGutterHelper** .


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
