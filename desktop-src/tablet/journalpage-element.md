---
description: Contém os detalhes sobre uma página individual em uma nota do diário.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829217"
---
# <a name="journalpage-element"></a>Elemento JournalPage

Contém os detalhes sobre uma página individual em uma nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos pai

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>Elementos filho

[**Estático**](stationery-element.md)

[**DocImage**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**Disputa**](content-element--journal-reader.md)

## <a name="attributes"></a>Atributos



| Atributo      | Type                      | Obrigatório | Descrição                                                                        | Valores possíveis                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Número**     | **xs:nonNegativeInteger** | Obrigatório | O número ordinal da página dentro do documento do diário, começando com um (1). | Qualquer inteiro não negativo.                                |
| **Largura**      | **xs:nonNegativeInteger** | Obrigatório | A largura da página.                                                             | Qualquer inteiro não negativo.                                |
| **Altura**     | **xs:nonNegativeInteger** | Obrigatório | A altura da página.                                                            | Qualquer inteiro não negativo.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Opcional | A altura da linha usada na página.                                           | Qualquer inteiro não negativo.                                |
| **LanguageId** | **xs:nonNegativeInteger** | Opcional | A ID de idioma usada para a página.                                                 | Um inteiro não negativo que representa uma ID de idioma válida. |



 

## <a name="element-information"></a>Informações do elemento



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| Tipo de elemento | ComplexType [**JournalPageType**](journalpagetype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                          |
| Nome do esquema  | Leitor de diário                                                      |



 

 

 



