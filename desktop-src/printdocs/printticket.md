---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105760297"
---
# <a name="printticket"></a>PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento PrintTicket é o elemento raiz do documento PrintTicket. Um elemento PrintTicket contém todas as informações de formatação de trabalho necessárias para gerar um trabalho.

## <a name="element-tag"></a>Marca do elemento

<PrintTicket>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML      | Detalhes                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica a versão do esquema que define os tipos de elemento e sua estrutura, um literal do tipo inteiro. A versão atual do esquema é "1". Esse atributo é necessário. <br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Category                   | Detalhes                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | Somente raiz do documento.<br/>                                                                                     |
| Elementos filho<br/>  | *Recurso* (zero ou mais)<br/> *ParameterInit* (zero ou mais)<br/> *Propriedade* (zero ou mais)<br/> |
| Este elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filho duplicados não são permitidos.<br/>                  |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

As dependências de configuração são aplicáveis somente a elementos em um documento de PrintCapabilities.

## <a name="example"></a>Exemplo

Consulte o [exemplo de PrintTicket](printticket-example.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




