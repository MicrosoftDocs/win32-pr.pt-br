---
description: O Tipo de Diretório do tipo semântico é um dos Tipos de Formato de Chave, que consiste em uma chave estrangeira na tabela Diretório fornecida pelo usuário.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ea91ceb9baaeb2c97883cace0266a146d80634ec07f5e25f0b01ac057c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251796"
---
# <a name="directory-type"></a>Tipo de diretório

O Tipo de Diretório [do tipo semântico](semantic-types.md) é um dos Tipos de Formato de Chave [,](key-format-types.md)que consiste em uma chave estrangeira na tabela [Diretório](directory-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um identificador Windows [instalador válido](identifier.md) para itens desse tipo. Mergemod.dll não impõe essa restrição e é responsabilidade da ferramenta de mesclagem garantir que o usuário fornece uma chave válida na tabela Diretório.

Um item configurável do tipo Diretório deve modificar apenas o diretório de destino da instalação e não modificar a imagem de origem. Um item configurável desse tipo deve, portanto, modificar apenas chaves estrangeiras para a tabela Directory e não modificar a tabela Directory diretamente.

Como a coluna Diretório da tabela Component não é anulada, null é um valor inválido para um item configurável desse tipo, mesmo que \_ o msmConfigItemNonNullable não seja definido na coluna Atributos. [](component-table.md)

O tipo De diretório pode ser usado com dois tipos de ContextData.

**IsolationDirectory ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um diretório de destino para arquivos no módulo. A ferramenta de mesclagem substitui o identificador do diretório nos modelos na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do diretório na coluna Nome, inserir "1" na coluna Formato, inserir "Diretório" na coluna Tipo e inserir "IsolationDirectory" na coluna ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md).

**ShortcutLocation ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um diretório de destino para atalhos no módulo. A ferramenta de mesclagem substitui o identificador do atalho nos modelos na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do diretório na coluna Nome, inserir "1" na coluna Formatar, inserir "Diretório" na coluna Tipo e inserir "ShortcutLocation" na coluna ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md).

 

 



