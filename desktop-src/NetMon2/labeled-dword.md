---
description: A estrutura LABELED DWORD define um rótulo que é exibido quando um valor de propriedade \_ DWORD específico é detectado.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: LABELED_DWORD (Netmon.h)
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
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364841"
---
# <a name="labeled_dword-structure"></a>Estrutura \_ DWORD ROTULADA

A **estrutura \_ LABELED DWORD** define um rótulo que é exibido quando um valor de propriedade DWORD específico é detectado.

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

Descrição textual ou rótulo que é exibido quando o valor DWORD especificado no **membro Value** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **membro lpLabeledDwordTable** da estrutura [SET](set.md) aponta para uma matriz  de estruturas **SET** que definem um ou mais membros de Rótulo dos pares de valor DWORD. Os pares são usados quando você deseja exibir um rótulo no lugar de um valor DWORD específico encontrado no pacote de protocolo.

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

 

 




