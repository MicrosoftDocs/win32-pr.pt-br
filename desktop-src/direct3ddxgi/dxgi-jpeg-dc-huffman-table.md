---
description: Descreve uma tabela de Huffman de DC JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Estrutura de DXGI_JPEG_DC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172975"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>\_Estrutura de \_ tabela de HUFFMAN de CD \_ \_ de dxgi JPEG2000

Descreve uma tabela de Huffman de DC JPEG.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**CodeCounts**
</dt> <dd>

O número de códigos para cada comprimento de código.

</dd> <dt>

**CodeValues**
</dt> <dd>

Os valores do código Huffman, em ordem de aumento do tamanho do código.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




