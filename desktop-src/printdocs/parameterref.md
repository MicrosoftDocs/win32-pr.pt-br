---
description: Saiba mais sobre o elemento ParameterRef, que define uma referência a um elemento ParameterInit e como ele funciona com ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407179"
---
# <a name="parameterref"></a>ParameterRef

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento ParameterRef define uma referência a um elemento ParameterInit. Um elemento ScoredProperty que contém um elemento ParameterRef não tem um elemento Value definido explicitamente. Em vez disso, o elemento ScoredProperty recebe seu valor do elemento ParameterInit referenciado por um elemento ParameterRef.

## <a name="element-tag"></a>Marca de elemento

<ParameterRef>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML   | Detalhes                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contém o atributo name do elemento ParameterDef referenciado dentro do contexto do documento atual.<br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Detalhes                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | Scoredproperty <br/>                                                                        |
| Elementos filho<br/>  | Nenhum permitido.<br/>                                                                        |
| Esse elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filhos duplicados não são permitidos.<br/> |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Os elementos ParameterRef podem não ter nenhuma dependência de configuração.

## <a name="example"></a>Exemplo

O exemplo a seguir ilustra como usar elementos ParameterRef para permitir que os usuários insiram parâmetros de tamanho de mídia personalizados.

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




