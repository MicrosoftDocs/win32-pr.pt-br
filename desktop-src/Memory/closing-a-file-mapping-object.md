---
description: Quando um processo termina com o objeto de mapeamento de arquivo, ele deve destruir todas as exibições de arquivo em seu espaço de endereço usando a função UnmapViewOfFile para cada exibição de arquivo.
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: Fechando um objeto de mapeamento de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828262"
---
# <a name="closing-a-file-mapping-object"></a>Fechando um objeto de mapeamento de arquivo

Quando um processo termina com o objeto de mapeamento de arquivo, ele deve destruir todas as exibições de arquivo em seu espaço de endereço usando a função [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) para cada exibição de arquivo.

Desmapear uma exibição mapeada de um arquivo invalida o intervalo ocupado pelo modo de exibição no espaço de endereço do processo e torna o intervalo disponível para outras alocações. Ele remove a entrada do conjunto de trabalho para cada página virtual não mapeada que faz parte do conjunto de trabalho do processo e reduz o tamanho do conjunto de trabalho do processo. Ele também decrementa a contagem de compartilhamento da página física correspondente.

As páginas modificadas na exibição não mapeada não são gravadas no disco até que sua contagem de compartilhamento chegue a zero ou, em outras palavras, até que elas sejam desmapeadas ou cortadas dos conjuntos de trabalho de todos os processos que compartilham as páginas. Mesmo assim, as páginas modificadas são gravadas "lentamente" em disco; ou seja, as modificações podem ser armazenadas em cache na memória e gravadas em disco posteriormente. Para minimizar o risco de perda de dados no caso de uma falha de energia ou de uma falha do sistema, os aplicativos devem liberar explicitamente as páginas modificadas usando a função [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Quando cada processo termina de usar o objeto de mapeamento de arquivo e tem todas as exibições não mapeadas, ele deve fechar o identificador do objeto de mapeamento de arquivo e o arquivo no disco chamando [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle). Essas chamadas para **CloseHandle** são realizadas com sucesso mesmo quando há exibições de arquivo que ainda estão abertas. No entanto, deixar as exibições de arquivo mapeadas causa vazamentos de memória.

 

 
