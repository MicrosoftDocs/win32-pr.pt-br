---
title: Estrutura XMUINT2
description: Descreve um vetor inteiro sem sinal 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2 estrutura HLSL
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
ms.openlocfilehash: 00ec040a848b3103b4d5070541f025ab9cfb0cfa
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222824"
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

Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` cabeçalho no SDK do DirectX (junho de 2010) para uso do C++. A versão mais recente desse cabeçalho no pacote NuGet [Microsoft. DXSDK. D3DX não o](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) define, e se baseia em [DirectX:: XMUINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint2) em DirectXMath em vez disso.



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Estruturas](format-conversion-structures.md)
</dt> <dt>

[Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
