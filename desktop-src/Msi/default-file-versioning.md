---
description: Os diagramas de fluxo nas seções a seguir ilustram as regras de controle de versão de arquivo padrão usadas quando o arquivo de chave de um componente que está sendo instalado tem o mesmo nome que um arquivo já instalado no local de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Controle de versão de arquivo padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c239cd7989308e79dbb0ee621241560ac33a7a049c83c0a44d2cb1c3c32f5fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039986"
---
# <a name="default-file-versioning"></a>Controle de versão de arquivo padrão

Os diagramas de fluxo nas seções a seguir ilustram as regras de controle de versão de arquivo padrão usadas quando o arquivo de chave de um componente que está sendo instalado tem o mesmo nome que um arquivo já instalado no local de destino. O controle de versão de arquivo padrão também é ilustrado na [substituição de arquivos existentes](replacing-existing-files.md).

observe que, com Windows Installer, o hash de arquivo está disponível para otimizar a cópia dos arquivos. Para obter detalhes, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e a [tabela MsiFileHash](msifilehash-table.md). A tabela MsiFileHash só pode ser usada com arquivos sem versão.

-   [Ambos os arquivos têm uma versão](both-files-have-a-version.md)
-   [Nenhum arquivo tem uma versão](neither-file-has-a-version.md)
-   [Nenhum arquivo tem uma versão com verificação de hash de arquivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Um arquivo tem uma versão](one-file-has-a-version.md)

 

 



