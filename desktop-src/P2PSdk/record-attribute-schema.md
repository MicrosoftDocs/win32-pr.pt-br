---
description: Os registros podem ter atributos específicos do aplicativo que são uma sequência de pares de nome ou valor representados como uma cadeia de caracteres XML no membro pszAttributes da estrutura de registro de mesmo nível \_ .
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Esquema de atributo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780489"
---
# <a name="record-attribute-schema"></a>Esquema de atributo de registro

Os registros podem ter atributos específicos do aplicativo que são uma sequência de pares de nome ou valor representados como uma cadeia de caracteres XML no membro **pszAttributes** da estrutura de [**\_ registro de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Os atributos são usados para filtrar uma pesquisa de registro iniciada por chamadas para [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), que usa um filtro de pesquisa XML especificado no [formato de consulta de pesquisa de registro](record-search-query-format.md) como um parâmetro.

Um atributo de registro pode ser um dos três tipos a seguir:

-   **int** é um valor inteiro.
-   **Date** é um valor DateTime representado como um dos formatos padrão descritos em [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   **String** é um valor de cadeia de caracteres Unicode.

A lista a seguir identifica os nomes de atributo específicos que são reservados pela infraestrutura de mesmo nível:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Exemplo de definição de atributos de registro

O exemplo de esquema a seguir mostra como definir atributos de registro:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> Os nomes de atributo devem ser sequências de caracteres alfanuméricos. Caracteres especiais como hifens ("-") e sublinhados (" \_ ") não são permitidos em um nome de atributo.

 

O exemplo a seguir de uma sequência de atributo XML contém os atributos **AuthenticationType** e **AuthExpires** personalizados que aparecem no membro **pszAttributes** do [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



