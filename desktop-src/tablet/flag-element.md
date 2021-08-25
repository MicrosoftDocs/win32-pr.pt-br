---
description: Contém um bitmap codificado em Base64 de um sinalizador associado à seção de uma nota do diário.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df40874178ba998ae9c864036b7befbf85179680de92cb68595f394e370e4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774076"
---
# <a name="flag-element"></a>Elemento Flag

Contém um bitmap codificado em Base64 de um sinalizador associado à seção de uma nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos pai

[**Conteúdo**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-------------------------------------------------------|
| Tipo de elemento | ComplexType de [**flagType**](flagtype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk            |
| Nome do esquema  | Leitor de diário                                        |



 

 

 



