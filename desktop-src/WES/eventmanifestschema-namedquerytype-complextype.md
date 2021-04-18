---
title: Tipo complexo NamedQueryType
description: Não usado. Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontradas. | Tipo complexo NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Log de eventos do tipo complexo NamedQueryType
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759767"
---
# <a name="namedquerytype-complex-type"></a>Tipo complexo NamedQueryType

Não usado. Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontradas.

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                       | Type                                                                             | Descrição                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**patternMaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) | Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.<br/> |



## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar o elemento [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) . Este exemplo usa o conteúdo da cadeia de caracteres de mensagem e o insere na cadeia de caracteres https://www .*. com.* Em seguida, ele substitui a cadeia de caracteres da mensagem pelo resultado. Por exemplo, se a cadeia de caracteres de mensagem contiver a Microsoft, a consulta substituiria a cadeia de caracteres de mensagem da Microsoft por https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





