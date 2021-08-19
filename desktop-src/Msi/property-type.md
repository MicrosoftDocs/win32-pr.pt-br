---
description: O Tipo de Propriedade do tipo semântico é um dos Tipos de Formato de Chave. Esse tipo consiste em uma chave estrangeira na tabela Propriedade fornecida pelo usuário.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6446b5a0ef5f2cf1bc969f531a3b8c35e6990a2ca3eee3c0002e4f62fbf4cea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145329"
---
# <a name="property-type"></a>Tipo de propriedade

O Tipo de Propriedade [do tipo semântico](semantic-types.md) é um dos Tipos [de Formato de Chave](key-format-types.md). Esse tipo consiste em uma chave estrangeira na [tabela Propriedade](property-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um identificador Windows [instalador válido](identifier.md) para itens desse tipo. Mergemod.dll não impõe essa restrição e é responsabilidade da ferramenta de mesclagem garantir que o usuário fornece uma chave válida na tabela Propriedade. As chaves primárias da tabela Property são os nomes de propriedade.

Null é um valor válido para esse tipo, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela [ModuleConfiguration](moduleconfiguration-table.md).

O Tipo de propriedade pode ser usado com os seguintes tipos de ContextData.

**ContextData Nulo**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um nome de propriedade para uma tabela de banco de dados no módulo. A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Propriedade" na coluna Tipo e deixar em branco a coluna ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md).

**Public ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça o nome de uma propriedade pública [para](public-properties.md) uma tabela de banco de dados no módulo. A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Propriedade" na coluna Tipo e inserir "Public" na coluna ContextData da tabela ModuleConfiguration.

**Private ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça o nome de uma propriedade privada [para](private-properties.md) uma tabela de banco de dados no módulo. A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Propriedade" na coluna Tipo e inserir "Particular" na coluna ContextData da tabela ModuleConfiguration.

 

 



