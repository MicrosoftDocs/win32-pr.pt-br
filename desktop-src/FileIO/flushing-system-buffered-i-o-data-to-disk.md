---
description: O Windows armazena os dados em operações de leitura e gravação de arquivo em buffers de dados mantidos pelo sistema para otimizar o desempenho do disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Liberando dados de e/s de System-Buffered para O disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506176"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Liberando dados de e/s de System-Buffered para O disco

O Windows armazena os dados em operações de leitura e gravação de arquivo em buffers de dados mantidos pelo sistema para otimizar o desempenho do disco. Quando um aplicativo grava em um arquivo, o sistema geralmente armazena em buffer os dados e grava os dados no disco regularmente. Um aplicativo pode forçar o sistema operacional a gravar o conteúdo desses buffers de dados no disco usando a função [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) . Como alternativa, um aplicativo pode especificar que as operações de gravação devem ignorar o buffer de dados e gravar diretamente no disco definindo o sinalizador de **arquivo sem sinalizador de \_ \_ \_ buffer** quando o arquivo é criado ou aberto usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

Se houver dados no buffer interno quando o arquivo for fechado, o sistema operacional não gravará automaticamente o conteúdo do buffer no disco antes de fechar o arquivo. Se o aplicativo não forçar o sistema operacional a gravar o buffer no disco antes de fechar o arquivo, o algoritmo de cache determina quando o buffer é gravado.

> [!Note]  
> O acesso a um buffer de dados enquanto uma operação de leitura ou gravação está usando ele pode corromper o buffer. Os aplicativos não devem ler, gravar no, realocar ou liberar o buffer de dados que uma operação de leitura ou gravação está usando até que a operação seja concluída.

 

 

 



