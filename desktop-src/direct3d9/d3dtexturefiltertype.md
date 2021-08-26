---
description: Define modos de filtragem de textura para um estágio de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeração D3DTEXTUREFILTERTYPE (D3D9Types.h)
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
ms.openlocfilehash: a9a55632ee1f1b8f2e40b1be1272411c7c24b3b18c576563ff9c0de7c79bc413
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069366"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Enumeração D3DTEXTUREFILTERTYPE

Define modos de filtragem de textura para um estágio de textura.

## <a name="syntax"></a>Syntax


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

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MIPFILTER,**](./d3dsamplerstatetype.md)desabilita o mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ POINT**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem de ponto deve ser usada como o filtro de ampliação ou minificação de textura, respectivamente. Quando usado com **D3DSAMP \_ MIPFILTER,** habilita mipmapping e especifica que o rasterizador escolhe a cor do texel do nível mip mais próximo.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ LINEAR**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem linear deve ser usada como o filtro de ampliação ou minificação de textura, respectivamente. Quando usado com **D3DSAMP \_ MIPFILTER,** habilita a filtragem mipmapping e trilinear; ele especifica que o rasterizador interpola entre os dois níveis de mip mais próximos.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANIS LTDA**
</dt> <dd>

Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem de textura anisotra usada como um filtro de ampliação ou minificação de textura, respectivamente. Compensa a distorção causada pela diferença no ângulo entre o polígono de textura e o plano da tela. O uso **com D3DSAMP \_ MIPFILTER** é indefinido.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Um filtro de amostra de 4 amostras usado como um filtro de ampliação ou minificação de textura. O uso [**com D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.

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

De definir o filtro de ampliação de um estágio de textura chamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o valor DE MAGFILTER de D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o \_ terceiro parâmetro.

Demarque o filtro de minificação de um estágio de textura chamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o valor MINFILTER de D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o \_ terceiro parâmetro.

Demarque o filtro de textura para usar níveis entre mipmap chamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o valor MIPFILTER de D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o \_ terceiro parâmetro.

Nem todos os modos de filtragem válidos para um dispositivo serão aplicados a mapas de volume. Em geral, os filtros de ampliação LINEAR D3DTEXF POINT e \_ D3DTEXF terão suporte para \_ mapas de volume. Se D3DPTEXTURECAPS MIPVOLUMEMAP estiver definido, o filtro mipmap D3DTEXF POINT e os filtros de \_ \_ \_ minificação LINEAR D3DTEXF POINT e D3DTEXF terão suporte para mapas de \_ volume. O dispositivo pode ou não dar suporte ao filtro Mipmap LINEAR D3DTEXF \_ para mapas de volume. Os dispositivos que suportam filtragem aniso nos mapas 2D não são necessariamente compatíveis com filtragem aniso nos mapas de volume. No entanto, os aplicativos que habilitam a filtragem anisuística receberão a melhor filtragem disponível (provavelmente linear) se não há suporte para filtragem anisoél.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
