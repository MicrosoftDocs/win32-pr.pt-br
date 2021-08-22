---
description: O Tipo de Arquivo do tipo semântico é um dos Tipos de Formato de Chave. Esse tipo consiste em uma chave estrangeira na tabela Arquivo fornecida pelo usuário.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7611cce64bfe036575ac611ebbf63406721085f75162b04e9163eb38840cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581746"
---
# <a name="file-type"></a>Tipo de arquivo

O Tipo de Arquivo do [tipo semântico](semantic-types.md) é um dos Tipos [de Formato de Chave](key-format-types.md). Esse tipo consiste em uma chave estrangeira na [tabela Arquivo](file-table.md) fornecida pelo usuário.

O Tipo de arquivo pode ser usado com os seguintes tipos de ContextData.

**AssemblyContext ContextData**

Esse tipo pode ser usado para permitir que os usuários configurem chaves estrangeiras para assemblies win32 ou common language runtime. A ferramenta de mesclagem deve substituir Windows [identificador](identifier.md) do instalador de dados para itens desse tipo no modelo na coluna Valor da tabela [ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll não impõe isso e é responsabilidade da ferramenta de mesclagem garantir que o usuário fornece uma chave válida na tabela Arquivo.

Null é um valor válido para esse tipo, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela [ModuleConfiguration](moduleconfiguration-table.md).

 

 



