---
title: Estrutura de D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Descreve os parâmetros usados para carregar uma textura de outra textura.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- Estrutura D3DX11_TEXTURE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989357"
---
# <a name="d3dx11_texture_load_info-structure"></a>\_Estrutura de \_ informações de carregamento de textura D3DX11 \_

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Descreve os parâmetros usados para carregar uma textura de outra textura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**pSrcBox**
</dt> <dd>

Tipo: **[ **\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Caixa de textura de origem (consulte a [**\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Caixa textura de destino (consulte a [**\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nível de mipmap de textura de origem, consulte [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obter mais detalhes.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nível de mipmap de textura de destino, consulte [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obter mais detalhes.

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de níveis de mipmap na textura de origem.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primeiro elemento da textura de origem.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primeiro elemento da textura de destino.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos a serem carregados.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opções de filtragem durante a reamostragem (consulte [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opções de filtragem ao gerar níveis MIP (consulte o [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada em uma chamada para [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).

Os valores padrão são:


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

