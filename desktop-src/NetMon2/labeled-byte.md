---
description: A estrutura \_ LABELED BYTE define um par BIT rotulado. O Rótulo do par BIT rotulado é exibido quando um valor de propriedade de byte específico é detectado.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: LABELED_BYTE (Netmon.h)
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
ms.openlocfilehash: 05aa29942768c0c40816eafce112f12a95cd0a713bebe612d2e5ad32776a33a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494976"
---
# <a name="labeled_byte-structure"></a>Estrutura DE \_ BYTE ROTULADA

A **estrutura \_ LABELED BYTE** define um par BIT rotulado. O **Rótulo** do par BIT rotulado é exibido quando um valor de propriedade de byte específico é detectado.

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

Valor BYTE da propriedade que você deseja detectar.

</dd> <dt>

**Rótulo**
</dt> <dd>

Descrição textual ou rótulo que é exibido quando o valor especificado no **membro Value** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **membro lpLabeledByteTable** da estrutura [SET](set.md) aponta para uma matriz  de estruturas **SET** que definem um ou mais membros de Rótulo dos pares de valores BYTE. Esses pares são usados quando você deseja exibir um rótulo no lugar de um valor BYTE específico encontrado no pacote de protocolo.

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

 

 




