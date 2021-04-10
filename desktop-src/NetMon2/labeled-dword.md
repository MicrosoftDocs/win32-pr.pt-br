---
description: A \_ estrutura DWORD rotulada define um rótulo que é exibido quando um valor específico da propriedade DWORD é detectado.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Estrutura de LABELED_DWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170659"
---
# <a name="labeled_dword-structure"></a>\_Estrutura DWORD rotulada

A estrutura **\_ DWORD rotulada** define um rótulo que é exibido quando um valor específico da propriedade DWORD é detectado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valor**
</dt> <dd>

Valor DWORD da propriedade que você deseja detectar.

</dd> <dt>

**Rótulo**
</dt> <dd>

Descrição textual ou rótulo que é exibido quando o valor DWORD especificado no membro **Value** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O membro **lpLabeledDwordTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais membros **Label** dos pares valor DWORD. Os pares são usados quando você deseja exibir um rótulo no lugar de um valor DWORD específico encontrado no pacote de protocolo.

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

 

 




