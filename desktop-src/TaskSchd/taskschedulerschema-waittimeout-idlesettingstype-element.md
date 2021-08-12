---
title: Elemento WaitTimeout (idleSettingsType)
description: Especifica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Agendador de Tarefas do elemento WaitTimeout
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d078acecf39f9bd4848cabaa8b203787049ca8a66e565e6183b8b1998389ad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610391"
---
# <a name="waittimeout-idlesettingstype-element"></a>Elemento WaitTimeout (idleSettingsType)

Especifica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa. Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas aguardará indefinidamente se uma condição ociosa ocorrer. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> . O tempo mínimo permitido é de 1 minuto.

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, essa configuração ociosa é especificada usando a propriedade [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .

Para desenvolvimento em C++, essa configuração ociosa é especificada usando a propriedade [**IIdleSettings:: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) .

## <a name="examples"></a>Exemplos

O XML a seguir define uma configuração ociosa que aguarda 24 horas para que uma condição ociosa ocorra.


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





