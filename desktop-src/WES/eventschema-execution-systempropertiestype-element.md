---
title: Elemento Execution (SystemPropertiesType)
description: Contém informações sobre o processo e o thread que registrou o evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Elemento de execução EventLog
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644364"
---
# <a name="execution-systempropertiestype-element"></a>Elemento Execution (SystemPropertiesType)

Contém informações sobre o processo e o thread que registrou o evento.

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O elemento **Execution** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome          | Tipo         | Descrição                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| Kerneltime    | unsignedInt  | Tempo de execução decorrido para instruções do modo kernel, em unidades de tempo de CPU.<br/>                        |
| ProcessID     | unsignedInt  | Identifica o processo que gerou o evento.<br/>                                               |
| Processador   | unsignedByte | O número de identificação do processador que processou o evento.<br/>                          |
| Processadortime | unsignedInt  | Para sessões privadas do ETW, o tempo de execução decorrido para as instruções do modo de usuário, em tiques de CPU.<br/> |
| SessionID     | unsignedInt  | O número de identificação da sessão do Terminal Server na qual o evento ocorreu.<br/>         |
| ThreadID      | unsignedInt  | Identifica o thread que gerou o evento.<br/>                                                |
| Usertime      | unsignedInt  | Tempo de execução decorrido para instruções do modo de usuário, em unidades de tempo de CPU.<br/>                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





