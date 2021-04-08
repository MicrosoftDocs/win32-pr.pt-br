---
description: O estado de instalação de um arquivo complementar não depende de suas próprias informações de controle de versão de arquivo, mas no controle de versão de seu pai complementar.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Arquivos complementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922250"
---
# <a name="companion-files"></a>Arquivos complementares

O estado de instalação de um arquivo complementar não depende de suas próprias informações de controle de versão de arquivo, mas no controle de versão de seu pai complementar. Consulte as [regras de controle de versão de arquivo](file-versioning-rules.md). Para especificar um arquivo complementar, a chave primária do pai complementar na tabela de [arquivos](file-table.md) deve ser criada na coluna versão do registro para o complemento.

No exemplo a seguir, fileA é o pai complementar e FileB é o arquivo complementar.

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Versão |
|-------|---------|
| FileA | 1.0.0.0 |
| FileB | FileA   |



 

Neste exemplo, o estado de instalação de FileB depende das [regras de controle de versão de arquivo](file-versioning-rules.md) e das informações de controle de versão do fileA. Se o instalador determinar que a versão do ArquivoA no pacote deve ser instalada em uma versão mais antiga do fileA que já existe no computador do usuário, ele também instalará o FileB do pacote, independentemente da versão de qualquer FileB instalado.

Observe que um arquivo que é o caminho de chave para seu componente não deve ser um arquivo complementar. Isso resultaria na lógica de controle de versão do arquivo de caminho de chave sendo determinado pelo arquivo pai complementar.

 

 



