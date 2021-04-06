---
description: A \_ estrutura LARGEINT rotulada define um rótulo que é exibido quando um valor de propriedade LARGEINT específico é detectado.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Estrutura de LABELED_LARGEINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011085"
---
# <a name="labeled_largeint-structure"></a>Estrutura de \_ LARGEINT rotulada

A estrutura **\_ LARGEINT rotulada** define um rótulo que é exibido quando um valor de propriedade LARGEINT específico é detectado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valor**
</dt> <dd>

Valor LARGEINT da propriedade que você deseja detectar.

</dd> <dt>

**Rótulo**
</dt> <dd>

Descrição textual ou rótulo que é exibido quando o valor de LARGEINT especificado no membro de **valor** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O membro **lpLabeledLargeIntTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais membros **Label** dos pares de valor LARGEINT. Os pares são usados quando você deseja exibir um rótulo no lugar de um valor de LARGEINT específico encontrado em um pacote de protocolo.

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

 

 




