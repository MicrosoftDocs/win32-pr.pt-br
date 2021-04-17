---
description: Com o armazenamento local de threads (TLS), você pode fornecer dados exclusivos para cada thread que o processo pode acessar usando um índice global. Um thread aloca o índice, que pode ser usado pelos outros threads para recuperar os dados exclusivos associados ao índice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Armazenamento local de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553826"
---
# <a name="thread-local-storage"></a>Armazenamento local de thread

Todos os threads de um processo compartilham seu espaço de endereço virtual. As variáveis locais de uma função são exclusivas para cada thread que executa a função. No entanto, as variáveis estática e global são compartilhadas por todos os threads no processo. Com o *armazenamento local de threads* (TLS), você pode fornecer dados exclusivos para cada thread que o processo pode acessar usando um índice global. Um thread aloca o índice, que pode ser usado pelos outros threads para recuperar os dados exclusivos associados ao índice.

A constante de \_ mínimo \_ de TLS disponível define o número mínimo de índices TLS disponíveis em cada processo. Esse mínimo é garantido como sendo pelo menos 64 para todos os sistemas. O número máximo de índices por processo é de 1.088.

Quando os threads são criados, o sistema aloca uma matriz de valores **LPVOID** para TLS, que são inicializados como NULL. Antes que um índice possa ser usado, ele deve ser alocado por um dos threads. Cada thread armazena seus dados para um índice TLS em um *slot TLS* na matriz. Se os dados associados a um índice couberem em um valor de **LPVOID** , você poderá armazenar os dados diretamente no slot TLS. No entanto, se você estiver usando um grande número de índices dessa forma, é melhor alocar armazenamento separado, consolidar os dados e minimizar o número de Slots TLS em uso.

O diagrama a seguir ilustra como o TLS funciona. Para obter um exemplo de código que ilustra o uso do armazenamento local de thread, consulte [usando o armazenamento local de thread](using-thread-local-storage.md).

![Diagrama que mostra como o processo do T L S funciona.](images/tls.png)

O processo tem dois threads, thread 1 e thread 2. Ele aloca dois índices para uso com TLS, gdwTlsIndex1 e gdwTlsIndex2. Cada thread aloca dois blocos de memória (um para cada índice) para armazenar os dados e armazena os ponteiros para esses blocos de memória nos slots TLS correspondentes. Para acessar os dados associados a um índice, o thread recupera o ponteiro para o bloco de memória do slot TLS e o armazena na variável local lpvData.

É ideal usar TLS em uma DLL (biblioteca de vínculo dinâmico). Para obter um exemplo, consulte [usando o armazenamento local de thread em uma biblioteca de vínculo dinâmico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Armazenamento local de threads (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Uso de armazenamento local de thread](using-thread-local-storage.md)
</dt> <dt>

[Usando o armazenamento local de threads em uma biblioteca de vínculo dinâmico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
