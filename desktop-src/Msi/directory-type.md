---
description: O tipo de diretório do tipo semântico é um dos tipos de formato de chave, que consiste em uma chave estrangeira na tabela de diretórios fornecida pelo usuário.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828998"
---
# <a name="directory-type"></a>Tipo de diretório

O tipo de diretório do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md), que consiste em uma chave estrangeira na tabela de [diretórios](directory-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo. Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de diretórios.

Um item configurável do tipo de diretório deve modificar apenas o diretório de destino da instalação e não modificar a imagem de origem. Um item configurável desse tipo deve, portanto, modificar apenas as chaves estrangeiras para a tabela de diretório e não modificar a tabela de diretório diretamente.

Como a \_ coluna Directory da [tabela Component](component-table.md) é não anulável, NULL é um valor inválido para um item configurável desse tipo, mesmo que msmConfigItemNonNullable não esteja definido na coluna Attributes.

O tipo de diretório pode ser usado com dois tipos de ContextData.

**IsolationDirectory ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um diretório de destino para arquivos no módulo. A ferramenta de mesclagem substitui o identificador do diretório nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do diretório na coluna nome, inserir "1" na coluna formato, inserir "diretório" na coluna tipo e digitar "IsolationDirectory" na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

**ShortcutLocation ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um diretório de destino para atalhos no módulo. A ferramenta de mesclagem substitui o identificador do atalho nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do diretório na coluna nome, inserir "1" na coluna formato, inserir "diretório" na coluna tipo e digitar "ShortcutLocation" na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

 

 



