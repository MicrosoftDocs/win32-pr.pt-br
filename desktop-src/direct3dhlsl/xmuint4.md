---
title: Estrutura XMUINT4
description: Descreve um vetor inteiro não assinado 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 estrutura HLSL
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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222844"
---
# <a name="xmuint4-structure"></a>Estrutura XMUINT4

Descreve um vetor inteiro não assinado 4D.

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

**z**
</dt> <dd>

componente z do vetor.

<dl> <dt>

**w**
</dt> <dd>

componente w do vetor.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Comentários

Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` cabeçalho no SDK do DirectX (junho de 2010) para uso do C++. A versão mais recente desse cabeçalho no pacote NuGet [Microsoft. DXSDK. D3DX não o](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) define, e se baseia em [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) em DirectXMath em vez disso.




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
