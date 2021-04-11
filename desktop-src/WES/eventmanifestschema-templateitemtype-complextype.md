---
title: Tipo complexo TemplateItemType
description: Um modelo que define os dados a serem incluídos com um evento. | Tipo complexo TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- Log de eventos do tipo complexo TemplateItemType
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172758"
---
# <a name="templateitemtype-complex-type"></a>Tipo complexo TemplateItemType

Um modelo que define os dados a serem incluídos com um evento.

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                   | Type                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**binary**](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | Reservado apenas para uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**dado**](eventmanifestschema-data-templateitemtype-element.md)         | [**Datadefinitiontype**](eventmanifestschema-datadefinitiontype-complextype.md)     | Define um item de dados que você deseja incluir com o evento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**struct**](eventmanifestschema-struct-templateitemtype-element.md)     | [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md) | Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento. Os provedores gravam a estrutura como um blob e não como membros individuais da estrutura.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) | [**XmlType**](eventmanifestschema-xmltype-complextype.md)                           | Um fragmento XML que é usado para renderizar os dados do evento. Se você não incluir o fragmento, os dados do evento serão renderizados na ordem em que os itens de dados são definidos no modelo. O conteúdo desse elemento é qualquer fragmento XML válido. O fragmento deve conter apenas um nó de nível superior e o nó de nível superior deve especificar seu próprio namespace. <br/> Para fazer referência a um item de dados no fragmento, defina o corpo do texto para um nó no fragmento como%*n*, em que *n* é o índice baseado em um dos itens de dados de nível superior na lista de itens de dados (você não pode fazer referência a membros de uma estrutura). O valor de índice especificado não deve ser maior que o número de itens de dados de nível superior no modelo.<br/> Esse elemento segue todos os elementos de **dados** e **struct** . <br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name | string | Reservado apenas para uso interno.<br/>                                                                                                                                                            |
| name | string | O nome do modelo.<br/>                                                                                                                                                                  |
| tid  | token  | Um identificador que identifica exclusivamente o modelo dentro da lista de modelos que o provedor define. Use esse nome para fazer referência ao modelo quando você definir sua definição de evento.<br/> |



## <a name="remarks"></a>Comentários

A definição do modelo deve ter pelo menos um elemento filho data ou struct. O provedor deve gravar os dados do evento na ordem dos itens de dados definidos no modelo.

O tamanho de todos os itens de dados no modelo deve ser inferior a 64 KB.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como criar uma definição de modelo.


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





