---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105780414"
---
# <a name="option"></a>Opção

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Option contém todos os elementos Property e ScoredProperty associados a essa opção.

## <a name="element-tag"></a>Marca do elemento

<Option>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML          | Detalhes                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| restrita<br/> | Esse atributo é opcional para um documento PrintCapabilities.<br/> Esse atributo indica se a opção está disponível para seleção ou uso. Esse atributo XML pode ser definido como um dos seguintes valores: None, PrintTicketSettings, AdminSetting ou DeviceSettings. <br/> Consulte [atributos XML](xml-attributes.md)<br/> |
| name<br/>        | Mantém o nome da opção, uma opção padrão ou uma opção definida de forma privada. O atributo XML é usado dessa forma para diferenciar as instâncias de opção. <br/>                                                                                                                                                        |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Category                   | Detalhes                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | Recurso <br/>                                                                                                                                                                                                                                                                              |
| Elementos filho<br/>  | *Propriedade* (zero ou mais)<br/> *ScoredProperty* (zero ou mais opções com o atributo XML ' name '; uma ou mais opções for que não utilizam o atributo XML ' name ' \* )<br/> \* somente as opções públicas definidas no esquema de impressão não podem ter nenhum atributo ' name ', como DocumentNUp)<br/> |
| Este elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filho duplicados não são permitidos.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Um elemento de definição de opção não pode ter nenhuma dependência de configuração.

## <a name="element-usage"></a>Uso do elemento

A finalidade do elemento Option é caracterizar um dos Estados que um atributo de configuração de dispositivo, representado por um elemento Feature, possa assumir. Cada definição de elemento de opção contém um ou mais elementos ScoredProperty que descrevem uma característica intrínseca ou essencial dessa opção. Para facilitar a portabilidade e a preservação da intenção, o esquema de impressão define muitos elementos de recursos comuns e uma variedade de elementos de opção para cada recurso. Portanto, é importante usar elementos de opção de impressão definidos pelo esquema, se possível, antes de criar suas próprias definições de opção. Entender o processo de definição de elementos de opção fornece informações úteis sobre o modo como os documentos e PrintCapabilities de impressão são usados nas arquiteturas do Microsoft .NET Framework versão 3,0 e do Windows Vista.

## <a name="example"></a>Exemplo

O exemplo a seguir define um nome para a opção.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




