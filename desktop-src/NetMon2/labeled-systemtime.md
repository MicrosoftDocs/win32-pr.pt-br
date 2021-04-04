---
description: A \_ estrutura SYSTEMTIME rotulada define um rótulo que é exibido quando um valor de Propriedade SYSTEMTIME específico é detectado.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Estrutura de LABELED_SYSTEMTIME (Netmon. h)
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
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837293"
---
# <a name="labeled_systemtime-structure"></a>Estrutura de \_ SYSTEMTIME rotulada

A estrutura **\_ SYSTEMTIME rotulada** define um rótulo que é exibido quando um valor de Propriedade SYSTEMTIME específico é detectado.

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

Descrição textual ou rótulo que é exibido quando o valor de SYSTEMTIME especificado no membro de **valor** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O membro **lpLabeledSystemTimeTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais pares rótulo Value. Os pares são usados quando você deseja exibir um rótulo no lugar de um valor de LARGEINT específico que é encontrado no pacote de protocolo.

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

 

 




