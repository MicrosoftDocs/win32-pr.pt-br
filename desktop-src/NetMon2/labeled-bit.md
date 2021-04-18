---
description: A estrutura de \_ bits rotulada define um par de bits de rótulo.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Estrutura de LABELED_BIT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750207"
---
# <a name="labeled_bit-structure"></a>Estrutura de \_ bits rotulada

A estrutura de **\_ bits rotulada** define um par de bits de rótulo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>Membros

<dl> <dt>

**BitNumber**
</dt> <dd>

Número de bits do par de bits de rótulo. Os valores variam de 0 a 255. Defina o membro **Bitnumber** como o bit usado na comparação do valor da propriedade.

</dd> <dt>

**LabelOff**
</dt> <dd>

Cadeia de caracteres ou rótulo exibido quando o BIT especificado em **BitNumber** é igual a zero. Por exemplo, um rótulo possível é "bit desativado".

</dd> <dt>

**Rotular**
</dt> <dd>

Cadeia de caracteres ou rótulo exibido quando o BIT especificado em **BitNumber** é igual a 1. Por exemplo, um rótulo possível é "bit em".

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma matriz de estruturas de **\_ bits rotuladas** é usada para definir um conjunto de pares de bits de rótulo. Um ponteiro para a matriz é especificado no membro **lpLabeledBit** da estrutura [set](set.md) . Os pares são usados quando você deseja exibir um rótulo com base na configuração de cada BIT. Normalmente, esse tipo de conjunto é usado para indicar o valor de ON ou OFF de BITs.

Quando um conjunto de bits é especificado, Monitor de Rede exibe somente os BITs incluídos na matriz de estruturas de **conjunto** . BITs que não estão na estrutura **definida** não são exibidos.

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

 

 




