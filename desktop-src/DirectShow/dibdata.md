---
description: A estrutura DIBDATA contém informações sobre um bitmap independente de dispositivo (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Estrutura DIBDATA (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: b4449f45afac56b202e9b23516dc849c6364e8781be7cfbe7cfb2b630bd16921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653813"
---
# <a name="dibdata-structure"></a>Estrutura DIBDATA

A `DIBDATA` estrutura contém informações sobre um bitmap independente de dispositivo (DIB) GDI.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**PaletteVersion**
</dt> <dd>

Esse membro deve ser incrementado sempre que a paleta for alterada.

</dd> <dt>

**DibSection**
</dt> <dd>

Estrutura **DIBSECTION** que contém informações sobre o DIB. Consulte a documentação do GDI para obter detalhes.

</dd> <dt>

**hBitmap**
</dt> <dd>

Identificador para o bitmap.

</dd> <dt>

**hMapping**
</dt> <dd>

Identificador para um objeto de mapeamento de arquivo usado para compartilhar memória entre GDI e um objeto [**CImageSample**](cimagesample.md) .

</dd> <dt>

**pBase**
</dt> <dd>

Endereço do bitmap.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl> |



 

 




