---
description: O Ícone Tipo de tipo semântico é um dos Tipos de Formato de Chave. Esse tipo consiste em uma chave na tabela Ícone fornecida pelo usuário.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28510eff674d1f25e632b1181943af70da73d9fc97a6a64ec5abd0807fe15cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634949"
---
# <a name="icon-type"></a>Tipo de ícone

O Ícone Tipo de [tipo semântico](semantic-types.md) é um dos Tipos [de Formato de Chave](key-format-types.md). Esse tipo consiste em uma chave na tabela [Ícone](icon-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um identificador Windows [instalador válido](identifier.md) para itens desse tipo. Mergemod.dll não impõe essa restrição e é responsabilidade da ferramenta de mesclagem garantir que o usuário fornece uma chave válida na tabela Ícone.

Null é um valor válido para esse tipo, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela [ModuleConfiguration](moduleconfiguration-table.md).

O tipo Binário pode ser usado com os seguintes tipos de ContextData.

**ShortcutIcon ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir [](icon-table.md) que o usuário forneça uma chave estrangeira para uma linha na Tabela de Ícones que contém uma imagem adequada para uso como um ícone de atalho. Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Ícone" na coluna Tipo e inserir "ShorcutIcon" na coluna ContextData da tabela ModuleConfiguration. Esse tipo não é apropriado para uso em uma tabela de interface do usuário. Para modificar uma chave para a tabela Ícone nessas tabelas, consulte Icon ContextData em [Tipo binário](binary-type.md).

 

 



