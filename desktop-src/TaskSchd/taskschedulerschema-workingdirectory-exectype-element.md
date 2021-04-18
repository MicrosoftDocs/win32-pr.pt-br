---
title: Elemento WorkingDirectory (exectype)
description: Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Agendador de Tarefas do elemento WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810446"
---
# <a name="workingdirectory-exectype-element"></a>Elemento WorkingDirectory (exectype)

Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

O elemento **WorkingDirectory** é definido pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                      | Derivado de                                                 | Descrição                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**exectype**](taskschedulerschema-exectype-complextype.md) | Especifica uma ação que executa uma operação de linha de comando.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, o diretório de trabalho é especificado pela propriedade [**execaction. WorkingDirectory**](execaction-workingdirectory.md) .

Para desenvolvimento em C++, o diretório de trabalho é especificado pela propriedade [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





