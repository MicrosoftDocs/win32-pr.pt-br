---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105762215"
---
# <a name="printcapabilities"></a>PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento PrintCapabilities representa a raiz do documento PrintCapabilities. O documento PrintCapabilities contém todas as informações necessárias para descrever os atributos de dispositivo com suporte, considerando uma configuração de dispositivo específica.

## <a name="element-tag"></a>Marca do elemento

<PrintCapabilities>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML      | Detalhes                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica a versão do esquema que define os tipos de elemento e sua estrutura. O atributo Version é do tipo inteiro. A versão do esquema atual é designada como "1". Esse atributo é necessário. <br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Category                   | Detalhes                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | Somente raiz do documento.<br/>                                                                                    |
| Elementos filho<br/>  | *Recurso* (zero ou mais)<br/> *ParameterDef* (zero ou mais)<br/> *Propriedade* (zero ou mais)<br/> |
| Este elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filho duplicados não são permitidos.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

O elemento raiz pode não ter nenhuma dependência de configuração.

## <a name="example"></a>Exemplo

Consulte o [exemplo de documento PrintCapabilities](printcapabilities-document-example.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




