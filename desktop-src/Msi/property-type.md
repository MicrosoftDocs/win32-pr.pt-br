---
description: O tipo de Propriedade do tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave estrangeira na tabela de propriedades fornecida pelo usuário.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010996"
---
# <a name="property-type"></a>Tipo de propriedade

O tipo de Propriedade do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md). Esse tipo consiste em uma chave estrangeira na [tabela de propriedades](property-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo. Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de propriedades. As chaves primárias da tabela de propriedades são os nomes de propriedade.

NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

O tipo de propriedade pode ser usado com os seguintes tipos de ContextData.

**ContextData nulo**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um nome de propriedade para uma tabela de banco de dados no módulo. A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "Property" na coluna type e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

**ContextData público**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça o nome de uma [propriedade pública](public-properties.md) a uma tabela de banco de dados no módulo. A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "Property" na coluna type e digitar "Public" na coluna ContextData da Tabela ModuleConfiguration.

**ContextData particular**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça o nome de uma [propriedade privada](private-properties.md) a uma tabela de banco de dados no módulo. A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "Property" na coluna type e inserir "Private" na coluna ContextData da Tabela ModuleConfiguration.

 

 



