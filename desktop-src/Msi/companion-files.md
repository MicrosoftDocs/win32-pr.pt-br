---
description: O estado de instalação de um arquivo complementar não depende de suas próprias informações de controle de versão de arquivo, mas no controle de versão de seu pai complementar.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Arquivos complementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d35aa89e216df4e17c84fb15c9c1f19908a74e9c1d14113da4df2128cdfb87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145095"
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

 

 



