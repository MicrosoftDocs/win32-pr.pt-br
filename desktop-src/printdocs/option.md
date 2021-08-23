---
description: Obter informações sobre o elemento Option. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f02f506c61353698bc4386541ea96dbf858790dd7c34c6d80b8dc2542c46a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098970"
---
# <a name="option"></a>Opção

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Option contém todos os elementos Property e ScoredProperty associados a essa opção.

## <a name="element-tag"></a>Marca de elemento

<Option>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML          | Detalhes                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Restrita<br/> | Esse atributo é opcional para um documento PrintCapabilities.<br/> Esse atributo indica se a Opção está disponível para seleção ou uso. Esse atributo XML pode ser definido como um dos seguintes valores: None, PrintTicketSettings, AdminSetting ou DeviceSettings. <br/> Consulte [Atributos XML](xml-attributes.md)<br/> |
| name<br/>        | Contém o nome da Opção, uma Opção padrão ou uma Opção definida de forma privada. O atributo XML é usado dessa maneira para diferenciar entre instâncias option. <br/>                                                                                                                                                        |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Detalhes                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | Recurso <br/>                                                                                                                                                                                                                                                                              |
| Elementos filho<br/>  | *Propriedade* (zero ou mais)<br/> *ScoredProperty* (zero ou mais opções com o atributo XML 'name'; uma ou mais opções para Opções que não utilizam o atributo XML 'name' \* )<br/> \* somente opções públicas definidas no Esquema de Impressão não podem ter nenhum atributo 'name', como DocumentNUp)<br/> |
| Esse elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filhos duplicados não são permitidos.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Um elemento option definition pode não ter nenhuma dependência de configuração.

## <a name="element-usage"></a>Uso do elemento

A finalidade do elemento Option é caracterizar um dos estados que um atributo de configuração de dispositivo, representado por um elemento Feature, pode assumir. Cada definição de elemento Option contém um ou mais elementos ScoredProperty que descrevem uma característica intrínseca ou essencial dessa Opção. Para facilitar a portabilidade e a preservação da intenção, o Esquema de Impressão define muitos elementos de recurso comuns e uma variedade de elementos Option para cada Recurso. Portanto, é importante usar elementos Print Schema-defined Option, se possível, antes de criar suas próprias definições de Opção. Entender o processo de definição de elementos Option fornece insights úteis sobre como o documento PrintCapabilities e PrintTickets são usados na arquitetura de impressão do Microsoft .NET Framework versão 3.0 e Windows Vista.

## <a name="example"></a>Exemplo

O exemplo a seguir define um nome para a Opção.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




