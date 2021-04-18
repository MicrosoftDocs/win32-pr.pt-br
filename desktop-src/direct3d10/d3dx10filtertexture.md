---
description: Gera cadeia de mipmap usando um filtro de textura específico.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Função D3DX10FilterTexture (D3DX10Tex. h)
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
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771628"
---
# <a name="d3dx10filtertexture-function"></a>Função D3DX10FilterTexture

Gera cadeia de mipmap usando um filtro de textura específico.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O nível de mipmap cujos dados são usados para gerar o restante da cadeia de mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Sinalizadores que controlam como cada MipLevel é filtrado (ou D3DX10 \_ padrão para a \_ caixa de filtro D3DX10 \_ ). Consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
