---
description: Encontre informações sobre o elemento ScoredProperty. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: Scoredproperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb600f3fa30c475f7bf28ab1e4c12b19875b6ef49e4f6f3537aead95bf47b999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033884"
---
# <a name="scoredproperty"></a>Scoredproperty

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento ScoredProperty declara uma propriedade que é intrínseca a uma definição option. Essas propriedades devem ser comparadas ao avaliar o quanto uma Opção solicitada corresponde a uma opção com suporte do dispositivo.

## <a name="element-tag"></a>Marca de elemento

<ScoredProperty>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML   | Detalhes                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contém o atributo name da ScoredProperty, uma propriedade padrão ou uma propriedade definida de forma privada. <br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Detalhes                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | *Opção*<br/> *Scoredproperty*<br/>                                                                                                                          |
| Elementos filho<br/>  | Você pode usar o<br/> *ParameterRef* (um)<br/> ou<br/> *Valor* (um)<br/> *Propriedade* (zero ou mais)<br/> *ScoredProperty* (zero ou mais)<br/> |
| Esse elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filhos duplicados não são permitidos.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Um elemento ScoredProperty pode não ter nenhuma dependência de configuração.

## <a name="example"></a>Exemplo

Declare um elemento ScoredProperty chamado MediaSizeWidth com um Valor de 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




