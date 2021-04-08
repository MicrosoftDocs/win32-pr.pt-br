---
description: O Windows dá suporte a operações de e/s de arquivo síncronas e assíncronas (sobrepostas) em recursos de comunicação serial.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Operações de leitura e gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089150"
---
# <a name="read-and-write-operations"></a>Operações de leitura e gravação

O Windows dá suporte a operações de e/s de arquivo síncronas e assíncronas (sobrepostas) em recursos de comunicação serial. Operações sobrepostas permitem que o thread de chamada execute outras tarefas enquanto a operação é executada em segundo plano. Um thread usa a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) para ler de um recurso de comunicação e a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ou [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) para gravar em um recurso de comunicação. O **ReadFile** e o **WriteFile** podem ser executados de forma síncrona ou assíncrona. **ReadFileEx** e **WriteFileEx** só podem ser executados de forma assíncrona.

O comportamento dessas funções de leitura e gravação é afetado pelo fato de a função ser executada como uma operação sobreposta, se os parâmetros de tempo limite estão associados ao identificador e se os parâmetros de controle de fluxo estão associados ao identificador.

Um thread também pode gravar em um recurso de comunicação usando a função [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) , que transmite um caractere especificado à frente de quaisquer dados pendentes no buffer de saída. Essa função é útil para transmitir um caractere de sinal de alta prioridade para o sistema de recebimento. A transmissão do caractere de prioridade alta ainda está sujeita ao controle de fluxo e tempo limite de gravação, e a operação é executada de forma síncrona.

Um thread pode usar a função [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) para descartar todos os caracteres na saída de um dispositivo ou no buffer de entrada. **PurgeComm** também pode encerrar operações de leitura ou gravação pendentes, mesmo que as operações não tenham sido concluídas. Se um thread usar **PurgeComm** para liberar um buffer de saída, os caracteres excluídos não serão transmitidos. Para esvaziar o buffer de saída ao garantir que o conteúdo seja transmitido, um thread pode chamar a função [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) (uma operação síncrona). Observe, no entanto, que **FlushFileBuffers** está sujeito ao controle de fluxo, mas não à gravação de tempos limite, e não retornará até que todas as operações de gravação pendentes tenham sido transmitidas.

 

 
