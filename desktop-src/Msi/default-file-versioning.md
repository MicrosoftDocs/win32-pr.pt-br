---
description: Os diagramas de fluxo nas seções a seguir ilustram as regras de controle de versão de arquivo padrão usadas quando o arquivo de chave de um componente que está sendo instalado tem o mesmo nome que um arquivo já instalado no local de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Controle de versão de arquivo padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829010"
---
# <a name="default-file-versioning"></a>Controle de versão de arquivo padrão

Os diagramas de fluxo nas seções a seguir ilustram as regras de controle de versão de arquivo padrão usadas quando o arquivo de chave de um componente que está sendo instalado tem o mesmo nome que um arquivo já instalado no local de destino. O controle de versão de arquivo padrão também é ilustrado na [substituição de arquivos existentes](replacing-existing-files.md).

Observe que, com Windows Installer, o hash de arquivo está disponível para otimizar a cópia dos arquivos. Para obter detalhes, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e a [tabela MsiFileHash](msifilehash-table.md). A tabela MsiFileHash só pode ser usada com arquivos sem versão.

-   [Ambos os arquivos têm uma versão](both-files-have-a-version.md)
-   [Nenhum arquivo tem uma versão](neither-file-has-a-version.md)
-   [Nenhum arquivo tem uma versão com verificação de hash de arquivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Um arquivo tem uma versão](one-file-has-a-version.md)

 

 



