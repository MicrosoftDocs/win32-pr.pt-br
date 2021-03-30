---
title: Otimização de arquivo composto
description: O armazenamento assíncrono permite que os aplicativos tenham layout preciso de arquivos compostos para que os dados estejam disponíveis na ordem em que os aplicativos o exigirão.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Otimização de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635135"
---
# <a name="compound-file-optimization"></a>Otimização de arquivo composto

O armazenamento assíncrono permite que os aplicativos tenham layout preciso de arquivos compostos para que os dados estejam disponíveis na ordem em que os aplicativos o exigirão. Se um aplicativo exigir apenas parte de seus dados para exibir uma primeira página de informações, esses dados poderão ser colocados no início do arquivo, mesmo se ele residir logicamente no final de um fluxo. Os dados de fluxos diferentes podem ser intercalados. Dados de áudio e vídeo, por exemplo, podem ser intercalados para que as operações de leitura subsequentes recuperem ambos simultaneamente, um requisito para aplicativos multimídia.

[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) pode ser usado para fazer layout de um DOCFILE, melhorando assim o desempenho na maioria dos cenários.

 

 




