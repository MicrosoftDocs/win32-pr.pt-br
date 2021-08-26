---
description: O Tipo Binário do tipo semântico é um dos Tipos de Formato de Chave. Esse tipo consiste em uma chave na tabela Binária fornecida pelo usuário.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Tipo binário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8412d63891f3028c1ef2beb8fa0e6a17c4a35c33df182cbd9f1059a593c50915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105366"
---
# <a name="binary-type"></a>Tipo binário

O Tipo Binário do tipo [semântico](semantic-types.md) é um dos Tipos [de Formato de Chave](key-format-types.md). Esse tipo consiste em uma chave na [tabela Binária](binary-table.md) fornecida pelo usuário.

A ferramenta de mesclagem deve substituir um identificador Windows [instalador válido](identifier.md) para itens desse tipo. Mergemod.dll não impõe essa restrição e é responsabilidade da ferramenta de mesclagem garantir que o usuário fornece uma chave válida na tabela Binária.

Null é um valor válido para esse tipo, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela [ModuleConfiguration](moduleconfiguration-table.md).

O tipo Binário pode ser usado com os seguintes tipos de ContextData.

**Bitmap ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na Tabela Binária que contém uma imagem de bitmap. Mergmod.dll garante nenhum tamanho específico ou tipo de bitmap e a ferramenta de mesclagem deve garantir que os dados são uma imagem válida. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Binário" na coluna Tipo e inserir "Bitmap" na coluna ContextData da tabela ModuleConfiguration.

**Ícone ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na Tabela Binária que contém uma imagem de ícone. Mergmod.dll não garante nenhum tamanho específico ou tipo de ícone e a ferramenta de mesclagem deve garantir que os dados são uma imagem válida. Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Binário" na coluna Tipo e inserir "Ícone" na coluna ContextData da tabela ModuleConfiguration. Esse tipo não é apropriado para uso em uma tabela de anúncio.

**EXE ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na Tabela Binária que contém uma imagem executável de 32 bits. Mergmod.dll não validar se os dados são válidos e a ferramenta de mesclagem deve garantir que os dados sejam um arquivo PE válido. Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Binário" na coluna Tipo e inserir "EXE" na coluna ContextData da tabela ModuleConfiguration.

**EXE64 ContextData**

Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na Tabela Binária que contém uma imagem executável de 32 bits ou de 64 bits. Mergmod.dll não validar se os dados são válidos e a ferramenta de mesclagem deve garantir que os dados sejam um arquivo PE válido. Para especificar um item configurável desse tipo, os autores do módulo devem inserir o nome do item configurável na coluna Nome, inserir "1" na coluna Formato, inserir "Binário" na coluna Tipo e inserir "EXE64" na coluna ContextData da tabela ModuleConfiguration.

 

 



