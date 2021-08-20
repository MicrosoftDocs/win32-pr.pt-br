---
description: Descreve uma tabela de Huffman de AC JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Estrutura de DXGI_JPEG_AC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 21e279e4974d221a6feba6f135343d122f30f3da1edb18210e0e14f92fdb94a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518369"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>Estrutura de tabela do DXGI \_ JPEG \_ AC- \_ HUFFMAN \_

Descreve uma tabela de Huffman de AC JPEG.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
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

 

 




