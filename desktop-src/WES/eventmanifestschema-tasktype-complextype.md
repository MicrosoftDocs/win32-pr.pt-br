---
title: Tipo complexo de TaskType
description: Define um componente ou subcomponente de um aplicativo. | Tipo complexo de TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType tipo complexo de log de eventos
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763752"
---
# <a name="tasktype-complex-type"></a>Tipo complexo de TaskType

Define um componente ou subcomponente de um aplicativo.

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                         | Type                                                                     | Descrição                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**opcodes**](eventmanifestschema-opcodes-tasktype-element.md) | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) | Define uma lista de opcodes específicos da tarefa. Você não pode usar os valores de opcode definidos em Winmeta.xml para opcodes específicos da tarefa.<br/> |



## <a name="attributes"></a>Atributos



| Nome      | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventGUID | [**GUIDtype**](eventmanifestschema-guidtype-simpletype.md)       | Um identificador global exclusivo, no formato de registro, que identifica a tarefa. Esse atributo é necessário se você usar o argumento-MOF de mensagens do compilador para gerar uma classe MOF para suporte de nível inferior.<br/>                                                                                                   |
| message   | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | O nome de exibição localizado para a tarefa. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto. <br/>                                                                                                   |
| name      | **QName**                                                         | O nome da tarefa.<br/>                                                                                                                                                                                                                                                                                 |
| símbolo    | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para fazer referência à tarefa em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para a tarefa no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |
| value     | [**UInt16type**](eventmanifestschema-hexint16type-simpletype.md) | Um valor numérico que identifica exclusivamente essa tarefa na lista de tarefas que o provedor define. O valor deve estar no intervalo de 1 a 239.<br/>                                                                                                                                             |



## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como especificar uma tarefa.


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





