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
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968547"
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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas](format-conversion-structures.md)
</dt> <dt>

[Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





