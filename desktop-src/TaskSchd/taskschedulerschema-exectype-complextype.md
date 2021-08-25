---
title: tipo complexo execType
description: Define os elementos filho e informações de sequenciamento do elemento Exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- tipo complexo execType Agendador de Tarefas
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e0726930f902ec0458f42fff9cdce39026cf63ddab92982bc30da33ca671712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796626"
---
# <a name="exectype-complex-type"></a>tipo complexo execType

Define os elementos filho e informações de sequenciamento do elemento [**Exec (actionGroup).**](taskschedulerschema-exec-actiongroup-element.md)

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type                                                        | Descrição                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](taskschedulerschema-arguments-exectype-element.md)               | **cadeia de caracteres**                                                  | Especifica os argumentos associados à operação de linha de comando. <br/>                              |
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | [**Pathtype**](taskschedulerschema-pathtype-simpletype.md) | Especifica o arquivo executável ou o documento a ser executado.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**Pathtype**](taskschedulerschema-pathtype-simpletype.md) | Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas complexos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





