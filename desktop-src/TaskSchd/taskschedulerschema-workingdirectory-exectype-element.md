---
title: Elemento WorkingDirectory (execType)
description: Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Elemento WorkingDirectory Agendador de Tarefas
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a91908d5cd774f19f32a182934688dc899179d1abba967b7871a646efcfe042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513736"
---
# <a name="workingdirectory-exectype-element"></a>Elemento WorkingDirectory (execType)

Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

O **elemento WorkingDirectory** é definido pelo [**tipo complexo execType.**](taskschedulerschema-exectype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                      | Derivado de                                                 | Descrição                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica uma ação que executa uma operação de linha de comando.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento de scripts, o diretório de trabalho é especificado pela [**propriedade ExecAction.WorkingDirectory.**](execaction-workingdirectory.md)

Para desenvolvimento em C++, o diretório de trabalho é especificado pela [**propriedade IExecAction::WorkingDirectory.**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)

## <a name="examples"></a>Exemplos

O XML a seguir define uma ação de execução.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





