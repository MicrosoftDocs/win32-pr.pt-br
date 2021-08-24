---
description: A estrutura LABELED LARGEINT define um rótulo que é exibido quando um valor de propriedade \_ LARGEINT específico é detectado.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: LABELED_LARGEINT (Netmon.h)
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
ms.openlocfilehash: fab2942a2a5188527c57663af0c6000aa2cb628eaa2499eef054854df9187784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778766"
---
# <a name="labeled_largeint-structure"></a>Estrutura LABELED \_ LARGEINT

A **estrutura LABELED \_ LARGEINT** define um rótulo que é exibido quando um valor de propriedade LARGEINT específico é detectado.

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

Descrição textual ou rótulo que é exibido quando o valor LARGEINT especificado no **membro Value** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **membro lpLabeledLargeIntTable** da estrutura [SET](set.md) aponta para uma matriz  de estruturas **SET** que definem um ou mais membros de Rótulo dos pares de valores LARGEINT. Os pares são usados quando você deseja exibir um rótulo no lugar de um valor LARGEINT específico encontrado em um pacote de protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




