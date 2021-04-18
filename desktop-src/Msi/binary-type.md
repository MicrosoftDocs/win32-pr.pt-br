---
description: O tipo binário de tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave na tabela binária fornecida pelo usuário.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Tipo de binário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505796"
---
# <a name="binary-type"></a>Tipo de binário

O tipo binário de [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md). Esse tipo consiste em uma chave na [tabela binária](binary-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo. Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela binária.

NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

O tipo binary pode ser usado com os seguintes tipos de ContextData.

**ContextData de bitmap**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na tabela binária que contém uma imagem de bitmap. Mergmod.dll não garante nenhum tamanho ou tipo de bitmap específico e a ferramenta de mesclagem deve garantir que os dados sejam uma imagem válida. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "binary" na coluna type e inserir "bitmap" na coluna ContextData da Tabela ModuleConfiguration.

**Ícone ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na tabela binária que contém uma imagem de ícone. Mergmod.dll não garante nenhum tamanho ou tipo de ícone específico e a ferramenta de mesclagem deve garantir que os dados sejam uma imagem válida. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "binary" na coluna type e digitar "Icon" na coluna ContextData da Tabela ModuleConfiguration. Esse tipo não é apropriado para uso em uma tabela de anúncio.

**ContextData EXE**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na tabela binária que contém uma imagem executável de 32 bits. Mergmod.dll não valida que os dados são válidos e a ferramenta de mesclagem deve garantir que os dados sejam um arquivo PE válido. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "binary" na coluna type e digitar "EXE" na coluna ContextData da Tabela ModuleConfiguration.

**EXE64 ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na tabela binária que contém uma imagem executável de 32 bits ou 64 bits. Mergmod.dll não valida que os dados são válidos e a ferramenta de mesclagem deve garantir que os dados sejam um arquivo PE válido. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "binary" na coluna type e inserir "EXE64" na coluna ContextData da Tabela ModuleConfiguration.

 

 



