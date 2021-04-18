---
title: Elemento RandomDelay (timetriggertype)
description: Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Elemento RandomDelay (timetriggertype)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Agendador de Tarefas do elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105810111"
---
# <a name="randomdelay-timetriggertype-element"></a>Elemento RandomDelay (timetriggertype)

Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

O elemento é definido pelo tipo complexo [**Timetriggertype**](taskschedulerschema-timetriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                    | Derivado de                                                               | Descrição                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**Gatilho de timetrigger (The Trigger)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade RandomDelay de ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).

Para desenvolvimento de script, consulte [**timetrigger. RandomDelay**](timetrigger-randomdelay.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





