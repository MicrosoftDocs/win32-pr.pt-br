---
description: Saiba mais sobre o elemento Value, que associa um literal a um tipo. O tipo de dados do valor deve ser String, Integer, decimal ou QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272bee4d7a5f88899f83e439d8e1630b4026713d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405979"
---
# <a name="value"></a>Valor

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Value associa um literal a um tipo.

## <a name="element-tag"></a>Marca do elemento

<Value>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML       | Detalhes                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Especifica o tipo de dados do valor, que deve ser um dos seguintes tipos definidos por XSD: String, Integer, Decimal, QName. Se ausente, o tipo de dados padrão é cadeia de caracteres.<br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Categoria                   | Detalhes                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | ParameterInit <br/> Propriedade<br/> ScoredProperty<br/>                                                                                   |
| Elementos filho<br/>  | Somente o conteúdo de caractere ou inteiro é permitido.<br/>                                                                                                |
| Este elemento<br/>    | O conteúdo nulo é permitido. O conteúdo do caractere deve estar em conformidade com a sintaxe definida pelo tipo de dados.<br/> Irmãos filho duplicados não são permitidos.<br/> |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Elementos de valor que aparecem no elemento ScoredProperty podem não ter nenhuma dependência de configuração. Elementos de valor que aparecem nos elementos de propriedade podem ter dependências arbitrárias na configuração.

## <a name="element-usage"></a>Uso do elemento

Um elemento Value pode aparecer dentro de um elemento Property ou ScoredProperty. A finalidade do elemento de valor é representar um valor como um tipo de dados XML padrão. O tipo de dados é especificado como um atributo XML do elemento de valor, xsi: Type. Observe que nem todos os tipos definidos por XSD ou definidos como XML têm suporte. Para obter uma lista de tipos com suporte, consulte [Resumo dos tipos de elementos](summary-of-element-types.md). Um elemento Value pode conter apenas o conteúdo de caractere. Nada mais pode aparecer como conteúdo em um elemento Value.

> [!Note]  
> Alguns elementos de propriedade definidos pelo esquema de impressão e ScoredProperty não contêm um elemento Value, pois sua finalidade é simplesmente ser pai de subpropriedades. Você não deve adicionar um elemento de valor a essas propriedades como essas, propriedades que não contêm um elemento de valor.

 

Para estar em conformidade com a estrutura de esquema de impressão, que exige que um elemento de valor ou subelementos estejam presentes nos elementos que dão suporte a valores, um valor ausente ou indefinido deve ser representado apresentando o elemento Value como um elemento vazio; ou seja, como <Value></Value>.

## <a name="example"></a>Exemplo

Defina um valor do tipo decimal e inicialize-o como "128,5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




