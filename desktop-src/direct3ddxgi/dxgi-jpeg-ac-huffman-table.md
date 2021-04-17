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
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764198"
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

 

 




