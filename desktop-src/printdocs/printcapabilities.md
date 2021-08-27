---
description: Saiba mais sobre o elemento PrintCapabilities, que representa a raiz do documento PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef035015e8024954b32d17dd87bab929221ac78
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883930"
---
# <a name="printcapabilities"></a>PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento PrintCapabilities representa a raiz do documento PrintCapabilities. O documento PrintCapabilities contém todas as informações necessárias para descrever os atributos de dispositivo com suporte, considerando uma configuração de dispositivo específica.

## <a name="element-tag"></a>Marca de elemento

&lt;PrintCapabilities&gt;

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML      | Detalhes                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica a versão do esquema que define tipos de elemento e sua estrutura. O atributo version é do tipo integer. A versão atual do esquema é designada como "1". Esse atributo é necessário. <br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Detalhes                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | Somente raiz do documento.<br/>                                                                                    |
| Elementos filho<br/>  | *Recurso* (zero ou mais)<br/> *ParameterDef* (zero ou mais)<br/> *Propriedade* (zero ou mais)<br/> |
| Esse elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Irmãos filhos duplicados não são permitidos.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

O elemento raiz pode não ter nenhuma dependência de configuração.

## <a name="example"></a>Exemplo

Consulte [Exemplo de documento PrintCapabilities](printcapabilities-document-example.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




