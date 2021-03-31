---
description: O tipo de enumeração do tipo semântico é um dos tipos de formato de texto.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921374"
---
# <a name="enum-type"></a>Tipo de enumeração

O tipo de enumeração do [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto escolhida pelo usuário a partir de um conjunto de opções. A ferramenta de mesclagem substitui a cadeia de caracteres selecionada selecionada nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, digitar "0" na coluna formato, digitar "enum" na coluna tipo e inserir a lista de possíveis cadeias de caracteres na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A lista de cadeias de caracteres possíveis deve ser fornecida como uma lista de cadeias de caracteres deliminated por ponto e vírgula. Cada opção deve estar no formato "nome = valor". Um ponto-e-vírgula literal pode ser adicionado ao valor prefixando o ponto e vírgula com um caractere de barra invertida. NULL é um valor válido, a menos que msmConfigItemNonNullable tenha sido incluído no campo Attributes da Tabela ModuleConfiguration.

 

 



