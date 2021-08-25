---
title: Estrutura XMUINT4
description: Descreve um vetor inteiro sem sinal 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- Estrutura XMUINT4 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932168d2d251d5506727503053cb56cab2e50e57209276649beb35932478ab26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981466"
---
# <a name="xmuint4-structure"></a>Estrutura XMUINT4

Descreve um vetor inteiro sem sinal 4D.

## <a name="syntax"></a>Sintaxe


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a>Membros

<dl> <dt>

**x**
</dt> <dd>

componente x do vetor.

</dd> <dt>

**y**
</dt> <dd>

componente y do vetor.

<dl> <dt>

**Z**
</dt> <dd>

z-component do vetor.

<dl> <dt>

**w**
</dt> <dd>

w-component do vetor.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Comentários

Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` header no SDK do DirectX (junho de 2010) para uso do C++. A versão mais recente desse header no Pacote NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) não o define mais e depende de [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) no DirectXMath.




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas](format-conversion-structures.md)
</dt> <dt>

[Desempacotar e empacotar formato DXGI \_ para In-Place edição de imagem](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>