---
description: O tipo de arquivo do tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave estrangeira na tabela de arquivos fornecida pelo usuário.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753269"
---
# <a name="file-type"></a>Tipo de arquivo

O tipo de arquivo do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md). Esse tipo consiste em uma chave estrangeira na [tabela de arquivos](file-table.md) fornecida pelo usuário.

O tipo de arquivo pode ser usado com os seguintes tipos de ContextData.

**AssemblyContext ContextData**

Esse tipo pode ser usado para permitir que os usuários configurem chaves estrangeiras para assemblies Win32 ou Common Language Runtime. A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer por itens desse tipo no modelo na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll não impõe isso e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de arquivos.

NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

 

 



