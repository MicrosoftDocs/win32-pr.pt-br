---
title: Estrutura XMUINT2
description: Descreve um vetor inteiro sem sinal 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- Estrutura XMUINT2 HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39ec30fd4966e46bd511729671c39653640fe3f8f858d74db96e59fa1f09d242
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067266"
---
# <a name="xmuint2-structure"></a>Estrutura XMUINT2

Descreve um vetor inteiro sem sinal 2D.

## <a name="syntax"></a>Sintaxe


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
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

</dd> </dl>



## <a name="remarks"></a>Comentários

Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` header no SDK do DirectX (junho de 2010) para uso do C++. A versão mais recente desse header no Pacote NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) não o define mais e depende de [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) no DirectXMath.



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