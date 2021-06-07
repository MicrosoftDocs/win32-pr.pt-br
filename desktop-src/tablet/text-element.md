---
description: Contém informações de texto da nota Diário.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432308"
---
# <a name="text-element"></a>Elemento Text

Contém informações de texto da nota Diário.

## <a name="definition"></a>Definição

Quando usado com [**Content**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Ou, quando usado com [**TitleInfo**](titleinfo-element.md) e [**GroupNode:**](groupnode-element.md)

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Elementos pai

[**Conteúdo**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos

Não há atributos quando usados com [**TitleInfo**](titleinfo-element.md) e [**GroupNode.**](groupnode-element.md) Quando usado com [**Content**](content-element--journal-reader.md), os atributos são os a seguir.



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais alto na caixa delimitada do elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitada para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitada para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|   Elemento           |   Valor                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento | [**ComplexType TextType**](texttype-complex-type.md) (com o elemento Content) **ou xs:string** (com [**elementos GroupNode**](groupnode-element.md) e [**TitleInfo)**](titleinfo-element.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink<br/>                                                                                                                                               |
| Nome do esquema  | Leitor de Diário<br/>                                                                                                                                                                           |



 

 

 




