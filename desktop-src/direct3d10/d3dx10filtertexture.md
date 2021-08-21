---
description: Gera a cadeia mipmap usando um filtro de textura específico.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Função D3DX10FilterTexture (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 225caf2c9b08a498e77723dbb7ab43c8fd4850262c1f58f5ae37a3157e953edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497636"
---
# <a name="d3dx10filtertexture-function"></a>Função D3DX10FilterTexture

Gera a cadeia mipmap usando um filtro de textura específico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

O objeto de textura a ser filtrado. Consulte [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O nível de mipmap cujos dados são usados para gerar o restante da cadeia mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Sinalizadores que controlam como cada miplevel é filtrado (ou D3DX10 \_ DEFAULT para D3DX10 \_ FILTER \_ BOX). Consulte [**SINALIZADOR DE FILTRO D3DX10 \_ \_**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
