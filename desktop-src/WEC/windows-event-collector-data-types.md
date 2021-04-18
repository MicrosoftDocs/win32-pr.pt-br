---
title: Tipos de dados do coletor de eventos do Windows (Evcoll. h)
description: Os tipos de dados do coletor de eventos do Windows são usados como tipos de variável de objeto de assinatura de evento, tipos de parâmetro de função e tipos de retorno de função.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796463"
---
# <a name="windows-event-collector-data-types"></a>Tipos de dados do coletor de eventos do Windows

Os tipos de dados do coletor de eventos do Windows são usados como tipos de variável de objeto de assinatura de evento, tipos de parâmetro de função e tipos de retorno de função.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**identificador do EC \_**
</dt> <dd>

Identificador para um objeto de assinatura. Usado para representar uma assinatura do coletor de eventos.

</dd> <dt>

**\_identificador de \_ propriedade da matriz de objetos do EC \_ \_**
</dt> <dd>

Identificador para uma matriz de valores de propriedade para as origens de evento de uma assinatura. O identificador de matriz é retornado pelo método [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) quando o valor de **EcSubscriptionEventSources** é passado para o parâmetro *PropertyId* .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





