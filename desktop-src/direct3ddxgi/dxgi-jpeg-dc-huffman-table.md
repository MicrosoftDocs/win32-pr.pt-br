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
ms.openlocfilehash: b431bbccb66bcb24e068229493ef87f2ac96736161bb306609ac4dd479dfb7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987116"
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

 

 




