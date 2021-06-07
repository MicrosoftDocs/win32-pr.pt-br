---
description: O elemento de nível superior em um arquivo XML de nota do diário.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432168"
---
# <a name="journaldocument-element"></a>Elemento JournalDocument

O elemento de nível superior em um arquivo XML de nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>Elementos pai

Nenhum.

## <a name="child-elements"></a>Elementos filho

[**Telas**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>Atributos



| Atributo             | Type                      | Obrigatório | Descrição                                                      | Valores possíveis           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Versão**           | **xs:string**             | Obrigatório | A versão do documento de diário representada no arquivo XML. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Obrigatório | A largura padrão da página para o documento do diário.          | Qualquer inteiro não negativo. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Obrigatório | A altura padrão da página para o documento do diário.         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|--------------------------------------------|
| Tipo de elemento | **JournalDocument**                        |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk |
| Nome do esquema  | Leitor de diário                             |



 

 

 



