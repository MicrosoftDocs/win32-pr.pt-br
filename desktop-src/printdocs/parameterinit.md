---
description: Saiba mais sobre o elemento ParameterInit, que define um valor para uma instância de um elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b961ede78b313e7fb3655024705a13f04edb947344493be4fe49ff14b5d00843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947852"
---
# <a name="parameterinit"></a>ParameterInit

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Define um valor para uma instância de um elemento ParameterDef. Um elemento ParameterInit é o destino da referência feita por um elemento ParameterRef.

## <a name="element-tag"></a>Marca de elemento

<ParameterInit>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML   | Detalhes                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contém o atributo name do elemento ParameterDef que deve ser inicializado dentro do contexto do documento atual.<br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Nome ou restrição                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | PrintTicket (raiz PrintTicket)<br/>                                                         |
| Elementos filho<br/>  | Valor (um)<br/>                                                                            |
| Esse elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filhos duplicados não são permitidos.<br/> |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Nenhum

## <a name="example"></a>Exemplo

O exemplo a seguir inicializa um parâmetro como 1. O exemplo em [ParameterDef](parameterdef.md) demonstra como definir todos os elementos property necessários para esse parâmetro.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




