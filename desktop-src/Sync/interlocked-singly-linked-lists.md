---
description: Uma lista vinculada isoladamente (SList) interbloqueada facilita a tarefa de inserção e exclusão de uma lista vinculada.
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: Listas vinculadas isoladamente interbloqueadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af39847fa2fd1b1873c661d6ec904783e0139b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771799"
---
# <a name="interlocked-singly-linked-lists"></a>Listas vinculadas isoladamente interbloqueadas

Uma *lista vinculada isoladamente (slist) interbloqueada* facilita a tarefa de inserção e exclusão de uma lista vinculada. Os SLists são implementados usando um algoritmo de não bloqueio para fornecer sincronização atômica, aumentar o desempenho do sistema e evitar problemas como inversão de prioridade e bloqueio comboios.

SLists são simples de implementar e usar no código de 32 bits. No entanto, é desafiador implementá-los no código de 64 bits porque a quantidade de dados intercambiáveis pelos primitivos de intercâmbio nativos interbloqueados não é o dobro do tamanho do endereço, pois ele está no código de 32 bits. Portanto, o SLists permite portar algoritmos escalonáveis de alto nível para o Windows.

**Windows 8:** A partir do Windows 8, os primitivos de intercâmbio nativos interligados apropriados estão disponíveis para o código de 64 bits, por exemplo, [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)).

Os aplicativos podem usar SLists chamando a função [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) para inicializar o cabeçalho da lista. Para inserir itens na lista, use a função [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) . Para excluir itens da lista, use a função [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) .

Todos os itens de lista devem ser alinhados em um limite de **\_ \_ alinhamento de alocação de memória** . Itens não alinhados podem causar resultados imprevisíveis. Confira **\_ \_ malloc alinhado**.

Para obter um exemplo, consulte [usando listas vinculadas individualmente](using-singly-linked-lists.md).

A tabela a seguir lista as funções SList.



| Função                                                         | Descrição                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | Inicializa o cabeçalho de uma lista vinculada individualmente.                                                                                                             |
| [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | Libera toda a lista de itens em uma lista vinculada individualmente.                                                                                                 |
| [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | Remove um item da frente de uma lista vinculada individualmente.                                                                                                   |
| [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | Insere um item na frente de uma lista vinculada individualmente.                                                                                                     |
| [**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))     | Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente.                                                                                  |
| [**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente. Esta versão do método não usa a Convenção de chamada **\_ \_ fastcall** . |
| [**RtlFirstEntrySList**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | Recupera a primeira entrada em uma lista vinculada individualmente.                                                                                                        |
| [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | Recupera o número de entradas na lista especificada vinculada individualmente.                                                                                      |



 

 

 
