---
description: Especifica o método usado para codificar as informações de vetor de movimento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Propriedade MFPKEY_DELTAMVRANGEINDEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a21ac1a0bdaf859c93bca800d72f5e9ed155919bb07a24f5287b2436e57f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113336"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>\_Propriedade MFPKEY DELTAMVRANGEINDEX

Especifica o método usado para codificar as informações de vetor de movimento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Se essa propriedade for definida, o codificador aumentará o intervalo de vetor de movimento Delta nos campos. As informações de vetor de movimento são válidas somente para campos entrelaçados.

Essa propriedade pode ser definida como um dos seguintes valores:



| Valor | Descrição                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Use o intervalo de vetor de movimento Delta existente.                                          |
| 1     | Dobrar o intervalo de vetor de movimento Delta na direção horizontal.                    |
| 2     | Dobrar o intervalo de vetor de movimento Delta na direção vertical.                      |
| 3     | Dobrar o intervalo de vetor de movimento Delta nas direções horizontal e vertical. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




