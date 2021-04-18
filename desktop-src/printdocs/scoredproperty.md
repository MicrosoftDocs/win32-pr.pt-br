---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105794001"
---
# <a name="scoredproperty"></a>ScoredProperty

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento ScoredProperty declara uma propriedade que é intrínseca a uma definição de opção. Essas propriedades devem ser comparadas ao avaliar a precisão com que uma opção solicitada corresponde a uma opção com suporte do dispositivo.

## <a name="element-tag"></a>Marca do elemento

<ScoredProperty>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML   | Detalhes                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Mantém o atributo Name de ScoredProperty, uma propriedade padrão ou uma propriedade definida de forma privada. <br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Categoria                   | Detalhes                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | *Opção*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Elementos filho<br/>  | Você pode usar o<br/> *ParameterRef* (um)<br/> ou<br/> *Valor* (um)<br/> *Propriedade* (zero ou mais)<br/> *ScoredProperty* (zero ou mais)<br/> |
| Este elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filho duplicados não são permitidos.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Um elemento ScoredProperty pode não ter nenhuma dependência de configuração.

## <a name="example"></a>Exemplo

Declare um elemento ScoredProperty chamado MediaSizeWidth com um valor de 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




