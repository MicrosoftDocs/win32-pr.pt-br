---
description: Define modos de filtragem de textura para um estágio de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeração D3DTEXTUREFILTERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343001"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Enumeração D3DTEXTUREFILTERTYPE

Define modos de filtragem de textura para um estágio de textura.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ nenhum**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), desabilita o mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**Ponto de D3DTEXF \_**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem de ponto deve ser usada como o filtro de ampliação ou de minificação de textura, respectivamente. Quando usado com **D3DSAMP \_ MIPFILTER**, habilita mipmapping e especifica que o rasterizador escolhe a cor do Texel do nível de MIP mais próximo.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ linear**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem linear deve ser usada como o filtro de ampliação ou de minificação de textura, respectivamente. Quando usado com **D3DSAMP \_ MIPFILTER**, habilita a filtragem de mipmapping e trilineion; ele especifica que o rasterizador interpola entre os dois níveis MIP mais próximos.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROPIC**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem de textura anisotropic usada como um filtro de ampliação ou de minificação de textura, respectivamente. Compensa a distorção causada pela diferença em ângulo entre o polígono da textura e o plano da tela. Use with **D3DSAMP \_ MIPFILTER** é indefinido.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Um filtro de tipo tenda de 4 amostras usado como um filtro de ampliação ou minificação de textura. Use with [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

Um filtro gaussiano de 4 amostras usado como um filtro de ampliação ou minificação de textura. O uso [**com D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

Filtro de convolução para texturas monocromáticas. Consulte [D3DFMT \_ A1](d3dformat.md).

Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

- Esse sinalizador está disponível apenas no Direct3D 9Ex.



 

O uso [**com D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

D3DTEXTUREFILTERTYPE é usado por [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) junto com [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para definir modos de filtragem de textura para um estágio de textura.

Para verificar se um formato dá suporte a tipos de filtro de textura diferentes de D3DTEXF POINT (que sempre tem suporte), chame \_ [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com D3DUSAGE \_ QUERY \_ FILTER.

De definir o filtro de ampliação de um estágio de textura chamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o valor DE MAGFILTER D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o \_ terceiro parâmetro.

Demarque o filtro de minificação de um estágio de textura chamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o valor MINFILTER de D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o \_ terceiro parâmetro.

Demarque o filtro de textura para usar níveis entre mipmap chamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o valor MIPFILTER de D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o \_ terceiro parâmetro.

Nem todos os modos de filtragem válidos para um dispositivo serão aplicados a mapas de volume. Em geral, os filtros de ampliação LINEAR D3DTEXF POINT e \_ D3DTEXF terão suporte para \_ mapas de volume. Se D3DPTEXTURECAPS \_ MIPVOLUMEMAP for definido, o filtro de \_ MIPMAP do D3DTEXF Point e os \_ filtros D3DTEXF Point e D3DTEXF \_ line linear terão suporte para mapas de volume. O dispositivo pode ou não dar suporte ao \_ filtro mipmap linear D3DTEXF para mapas de volume. Os dispositivos que dão suporte à filtragem de anisotropic para mapas 2D não necessariamente dão suporte à filtragem de anisotropic para mapas de volume. No entanto, os aplicativos que habilitam a filtragem de anisotropic receberão a melhor filtragem disponível (provavelmente linear) se não houver suporte para a filtragem de anisotropic.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
