---
description: A estrutura de \_ palavras rotulada define um rótulo que é exibido quando um valor de propriedade de palavra específico é detectado.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Estrutura de LABELED_WORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754315"
---
# <a name="labeled_word-structure"></a>Estrutura de \_ palavras rotulada

A estrutura de **\_ palavras rotulada** define um rótulo que é exibido quando um valor de propriedade de palavra específico é detectado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valor**
</dt> <dd>

Valor de palavra da propriedade que você deseja detectar.

</dd> <dt>

**Rótulo**
</dt> <dd>

Descrição textual ou rótulo que é exibido quando o valor de palavra especificado no membro de **valor** é detectado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O membro **lpLabeledWordTable** da estrutura [set](set.md) aponta para uma matriz de estruturas set para definir um ou mais pares rótulo Value. Esses pares são usados quando você deseja exibir um rótulo no lugar de um valor de palavra específico encontrado em um pacote de protocolo.

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

 

 




