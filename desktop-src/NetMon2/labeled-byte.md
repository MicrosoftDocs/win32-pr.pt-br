---
description: A estrutura de \_ bytes rotulada define um par de bits rotulado. O rótulo do par de bits rotulado é exibido quando um valor de propriedade de byte específico é detectado.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Estrutura de LABELED_BYTE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752232"
---
# <a name="labeled_byte-structure"></a>Estrutura de \_ bytes rotulada

A estrutura de **\_ bytes rotulada** define um par de bits rotulado. O **rótulo** do par de bits rotulado é exibido quando um valor de propriedade de byte específico é detectado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valor**
</dt> <dd>

Valor de BYTE da propriedade que você deseja detectar.

</dd> <dt>

**Rótulo**
</dt> <dd>

Descrição textual ou rótulo que é exibido quando o valor especificado no membro de **valor** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O membro **lpLabeledByteTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais membros **Label** dos pares de valor de byte. Esses pares são usados quando você deseja exibir um rótulo no lugar de um valor de BYTE específico encontrado no pacote de protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




