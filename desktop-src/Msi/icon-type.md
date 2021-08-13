---
description: O tipo de ícone de tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave na tabela de ícones fornecida pelo usuário.
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

O tipo de ícone de [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md). Esse tipo consiste em uma chave na [tabela de ícones](icon-table.md) fornecida pelo usuário.

a ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo. Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de ícones.

NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

O tipo binary pode ser usado com os seguintes tipos de ContextData.

**ShortcutIcon ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na [tabela de ícones](icon-table.md) que contém uma imagem adequada para uso como um ícone de atalho. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, digitar "Icon" na coluna type e digitar "ShorcutIcon" na coluna ContextData da Tabela ModuleConfiguration. Esse tipo não é apropriado para uso em uma tabela de interface do usuário. Para modificar uma chave para a tabela de ícones nessas tabelas, consulte o ícone ContextData em [tipo binário](binary-type.md).

 

 



