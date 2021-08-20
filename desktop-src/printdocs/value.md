---
description: Saiba mais sobre o elemento Value, que associa um literal a um tipo. O tipo de dados Value deve ser string, integer, decimal ou QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739ce465408d1cd1447de5aeac2e314e879f48f69f13735855e628c8901c2c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685857"
---
# <a name="value"></a>Valor

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Value associa um literal a um tipo.

## <a name="element-tag"></a>Marca de elemento

<Value>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML       | Detalhes                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Especifica o tipo de dados Value, que deve ser um dos seguintes tipos definidos por XSD: cadeia de caracteres, inteiro, decimal, QName. Se estiver ausente, o tipo de dados padrão será cadeia de caracteres.<br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Detalhes                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | ParameterInit <br/> Propriedade<br/> Scoredproperty<br/>                                                                                   |
| Elementos filho<br/>  | Somente o conteúdo de caractere ou inteiro é permitido.<br/>                                                                                                |
| Esse elemento<br/>    | O conteúdo nulo é permitido. O conteúdo do caractere deve estar em conformidade com a sintaxe definida pelo tipo de dados.<br/> Irmãos filhos duplicados não são permitidos.<br/> |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Os elementos de valor que aparecem dentro do elemento ScoredProperty podem não ter nenhuma dependência de configuração. Os elementos de valor que aparecem nos elementos Property podem ter dependências arbitrárias na configuração.

## <a name="element-usage"></a>Uso do elemento

Um elemento Value pode aparecer dentro de um elemento Property ou ScoredProperty. A finalidade do elemento Value é representar um valor como um tipo de dados XML padrão. O tipo de dados é especificado como um atributo XML do elemento Value, xsi:type. Observe que nem todos os tipos definidos por XSD ou XML são suportados. Para ver uma lista de tipos com suporte, consulte [Resumo dos tipos de elemento](summary-of-element-types.md). Um elemento Value pode conter apenas o conteúdo do caractere. Nada mais pode aparecer como conteúdo em um elemento Value.

> [!Note]  
> Alguns elementos Print Schema-defined Property e ScoredProperty não contêm um elemento Value, porque sua finalidade é simplesmente ser pais de subpropriedades. Você não deve adicionar um elemento Value a propriedades como essas, propriedades que não contêm um elemento Value.

 

Para estar em conformidade com a Estrutura de Esquema de Impressão, que requer que um elemento Value ou subelementos esteja presente nos elementos que suportam valores, um valor ausente ou indefinido deve ser representado apresentando o elemento Value como um elemento vazio; ou seja, como <Value></Value>.

## <a name="example"></a>Exemplo

Defina um Valor do tipo decimal e inicialize-o como "128,5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




