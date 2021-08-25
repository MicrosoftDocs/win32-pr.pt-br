---
description: O Tipo de Enum do tipo semântico é um dos Tipos de Formato de Texto.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo Enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c5df6b0f76cc789c148e841827a75e7184aca2892d7d6e2233843e26aac80f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869316"
---
# <a name="enum-type"></a>Tipo Enum

O Tipo de Enum do [tipo semântico](semantic-types.md) é um dos Tipos [de Formato de Texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto escolhida pelo usuário de um conjunto de opções. A ferramenta de mesclagem substitui a cadeia de caracteres selecionada nos modelos especificados na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de caracteres de texto na coluna Nome, inserir "0" na coluna Formato, inserir "Enum" na coluna Tipo e inserir a lista de possíveis cadeias de caracteres na coluna ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md). A lista de cadeias de caracteres possíveis deve ser fornecida como uma lista de cadeias de caracteres delimitadas por ponto e vírgula. Cada opção deve estar no formato "Name=Value". Um ponto e vírgula literal pode ser adicionado ao valor prefixando o ponto e vírgula com um caractere de faixa invertida. Null é um valor válido, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela ModuleConfiguration.

 

 



