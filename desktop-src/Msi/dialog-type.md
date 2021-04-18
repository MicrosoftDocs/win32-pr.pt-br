---
description: O tipo de caixa de diálogo do tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave estrangeira na tabela de diálogo fornecida pelo usuário.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo de Caixa de Diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778725"
---
# <a name="dialog-type"></a>Tipo de Caixa de Diálogo

O tipo de caixa de diálogo do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md). Esse tipo consiste em uma chave estrangeira na [tabela de diálogo](dialog-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo. Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de diálogo.

NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

O tipo de caixa de diálogo pode ser usado com os seguintes tipos de ContextData.

**DialogNext ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira na tabela de diálogo. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna nome, inserir "1" na coluna de formato, inserir "caixa de diálogo" na coluna tipo e digitar "DialogNext" na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

**DialogPrev ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira na tabela de diálogo. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna nome, inserir "1" na coluna de formato, inserir "caixa de diálogo" na coluna tipo e digitar "DialogPrev" na coluna ContextData da Tabela ModuleConfiguration.

 

 



