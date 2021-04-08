---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contém um valor que indica o comprimento do atraso para uma hora de início da tarefa quando uma alteração de estado de sessão Terminal Server é detectada.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Elemento Delay Agendador de Tarefas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086455"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>Elemento Delay (sessionStateChangeTriggerType)

Contém um valor que indica o comprimento do atraso para uma hora de início da tarefa quando uma alteração de estado de sessão Terminal Server é detectada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

O elemento **Delay** é definido pelo tipo complexo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                       | Derivado de                                                                                           | Descrição                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado. <br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o atraso de gatilho de alteração de estado de sessão é especificado usando a propriedade [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .

Para desenvolvimento em C++, o atraso de gatilho de alteração de estado de sessão é especificado usando a [**Propriedade Delay de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





