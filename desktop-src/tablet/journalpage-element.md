---
description: Contém os detalhes sobre uma página individual em uma nota de Diário.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432138"
---
# <a name="journalpage-element"></a>Elemento JournalPage

Contém os detalhes sobre uma página individual em uma nota de Diário.

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

[**Conteúdo**](content-element--journal-reader.md)

## <a name="attributes"></a>Atributos



| Atributo      | Type                      | Obrigatório | Descrição                                                                        | Valores possíveis                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Número**     | **xs:nonNegativeInteger** | Obrigatório | O número ordinal da página dentro do documento Diário, começando com um (1). | Qualquer inteiro não negativo.                                |
| **Largura**      | **xs:nonNegativeInteger** | Obrigatório | A largura da página.                                                             | Qualquer inteiro não negativo.                                |
| **Altura**     | **xs:nonNegativeInteger** | Obrigatório | A altura da página.                                                            | Qualquer inteiro não negativo.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Opcional | A altura da linha usada na página.                                           | Qualquer inteiro não negativo.                                |
| **Languageid** | **xs:nonNegativeInteger** | Opcional | A ID de idioma usada para a página.                                                 | Um inteiro não negativo que representa uma ID de idioma válida. |



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|---------------------------------------------------------------------|
| Tipo de elemento | [**ComplexType JournalPageType**](journalpagetype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                          |
| Nome do esquema  | Leitor de Diário                                                      |



 

 

 



