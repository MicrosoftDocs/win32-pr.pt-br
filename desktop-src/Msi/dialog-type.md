---
description: O Tipo de caixa de diálogo do tipo semântico é um dos Tipos de Formato de Chave. Esse tipo consiste em uma chave estrangeira na tabela Diálogo fornecida pelo usuário.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo de Caixa de Diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f945b499cfab5ca8b3bf85180c16d9be88f4093b258513a11b5059874cb403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764016"
---
# <a name="dialog-type"></a>Tipo de Caixa de Diálogo

O Tipo de caixa de diálogo [do tipo semântico](semantic-types.md) é um dos [Tipos de Formato de Chave](key-format-types.md). Esse tipo consiste em uma chave estrangeira na tabela [Diálogo](dialog-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um identificador Windows [instalador válido](identifier.md) para itens desse tipo. Mergemod.dll não impõe essa restrição e é responsabilidade da ferramenta de mesclagem garantir que o usuário fornece uma chave válida na tabela Diálogo.

Null é um valor válido para esse tipo, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela [ModuleConfiguration](moduleconfiguration-table.md).

O tipo dialog pode ser usado com os seguintes tipos de ContextData.

**DialogNext ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira na Tabela de Diálogo. Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Diálogo" na coluna Tipo e inserir "DialogNext" na coluna ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md).

**DialogPrev ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira na Tabela de Diálogo. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Diálogo" na coluna Tipo e inserir "DialogPrev" na coluna ContextData da tabela ModuleConfiguration.

 

 



