---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172549"
---
# <a name="parameterinit"></a>ParameterInit

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Define um valor para uma instância de um elemento ParameterDef. Um elemento ParameterInit é o destino da referência feita por um elemento ParameterRef.

## <a name="element-tag"></a>Marca do elemento

<ParameterInit>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML   | Detalhes                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Mantém o atributo Name do elemento ParameterDef que deve ser inicializado dentro do contexto do documento atual.<br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Category                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | PrintTicket (raiz do PrintTicket)<br/>                                                         |
| Elementos filho<br/>  | Valor (um)<br/>                                                                            |
| Este elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filho duplicados não são permitidos.<br/> |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Nenhum

## <a name="example"></a>Exemplo

O exemplo a seguir inicializa um parâmetro para 1. O exemplo em [ParameterDef](parameterdef.md) demonstra como definir todos os elementos de propriedade necessários para esse parâmetro.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




