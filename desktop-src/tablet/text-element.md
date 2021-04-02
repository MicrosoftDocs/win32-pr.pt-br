---
description: Contém informações de texto da nota do diário.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922645"
---
# <a name="text-element"></a>Elemento Text

Contém informações de texto da nota do diário.

## <a name="definition"></a>Definição

Quando usado com o [**conteúdo**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Ou, quando usado com [**TitleInfo**](titleinfo-element.md) e [**GroupNode**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Elementos pai

[**Disputa**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos

Não há atributos quando usados com [**TitleInfo**](titleinfo-element.md) e [**GroupNode**](groupnode-element.md). Quando usado com [**conteúdo**](content-element--journal-reader.md), os atributos são os seguintes.



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Mantida**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento | [**Tipo**](texttype-complex-type.md) complexType (com o elemento Content) ou **xs: String** (com elementos [**GroupNode**](groupnode-element.md) e [**TitleInfo**](titleinfo-element.md) ) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk<br/>                                                                                                                                               |
| Nome do esquema  | Leitor de diário<br/>                                                                                                                                                                           |



 

 

 




