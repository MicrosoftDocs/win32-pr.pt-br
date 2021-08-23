---
description: A estrutura LABELED SYSTEMTIME define um rótulo que é exibido quando um valor específico da propriedade \_ SYSTEMTIME é detectado.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: LABELED_SYSTEMTIME (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 94ce2a2e0b86c24ea6c16627fd0b866e18aaf48f3c1f0b318a601809e1ee03dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742706"
---
# <a name="labeled_systemtime-structure"></a>Estrutura \_ SYSTEMTIME ROTULADA

A **estrutura \_ LABELED SYSTEMTIME** define um rótulo que é exibido quando um valor específico da propriedade SYSTEMTIME é detectado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valor**
</dt> <dd>

Valor SYSTEMTIME de uma propriedade que você deseja detectar.

</dd> <dt>

**Rótulo**
</dt> <dd>

Descrição textual ou rótulo que é exibido quando o valor SYSTEMTIME especificado no **membro Value** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **membro lpLabeledSystemTimeTable** da estrutura [SET](set.md) aponta para uma matriz de estruturas **SET** que definem um ou mais pares de valores de rótulo. Os pares são usados quando você deseja exibir um rótulo no lugar de um valor LARGEINT específico encontrado no pacote de protocolo.

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

 

 




