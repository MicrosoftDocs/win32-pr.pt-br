---
description: Com o armazenamento local do thread (TLS), você pode fornecer dados exclusivos para cada thread que o processo pode acessar usando um índice global. Um thread aloca o índice, que pode ser usado pelos outros threads para recuperar os dados exclusivos associados ao índice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Armazenamento local de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32c1630fb5690fc3ade4d319e7787c5287b27c270a9b43e3825e547e68bd4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792991"
---
# <a name="thread-local-storage"></a>Armazenamento local de thread

Todos os threads de um processo compartilham seu espaço de endereço virtual. As variáveis locais de uma função são exclusivas para cada thread que executa a função. No entanto, as variáveis estáticas e globais são compartilhadas por todos os threads no processo. Com *o armazenamento local do thread* (TLS), você pode fornecer dados exclusivos para cada thread que o processo pode acessar usando um índice global. Um thread aloca o índice, que pode ser usado pelos outros threads para recuperar os dados exclusivos associados ao índice.

A constante TLS MINIMUM AVAILABLE define o número mínimo de \_ \_ índices TLS disponíveis em cada processo. Esse mínimo é garantido como pelo menos 64 para todos os sistemas. O número máximo de índices por processo é 1.088.

Quando os threads são criados, o sistema aloca uma matriz de valores **LPVOID** para TLS, que são inicializados como NULL. Antes que um índice possa ser usado, ele deve ser alocado por um dos threads. Cada thread armazena seus dados para um índice TLS em um *slot TLS* na matriz. Se os dados associados a um índice se ajustarem a um valor **LPVOID,** você poderá armazenar os dados diretamente no slot TLS. No entanto, se você estiver usando um grande número de índices dessa maneira, é melhor alocar armazenamento separado, consolidar os dados e minimizar o número de slots TLS em uso.

O diagrama a seguir ilustra como o TLS funciona. Para ver um exemplo de código que ilustra o uso do armazenamento local do thread, consulte [Usando o thread local Armazenamento](using-thread-local-storage.md).

![Diagrama que mostra como funciona o processo de T L S.](images/tls.png)

O processo tem dois threads, Thread 1 e Thread 2. Ele aloca dois índices para uso com TLS, gdwTlsIndex1 e gdwTlsIndex2. Cada thread aloca dois blocos de memória (um para cada índice) no qual armazenar os dados e armazena os ponteiros para esses blocos de memória nos slots TLS correspondentes. Para acessar os dados associados a um índice, o thread recupera o ponteiro para o bloco de memória do slot TLS e os armazena na variável local lpvData.

É ideal usar o TLS em uma DLL (biblioteca de vínculo dinâmico). Para ver um exemplo, consulte [Using Thread Local Armazenamento in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Thread Local Armazenamento (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Uso de armazenamento local de thread](using-thread-local-storage.md)
</dt> <dt>

[Usando o thread local Armazenamento em uma biblioteca de vínculo dinâmico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
