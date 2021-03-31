---
title: Rotinas de conclusão de HTTP
description: Os aplicativos têm várias opções para receber indicações de conclusão e fornecer alguma flexibilidade para os desenvolvedores.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee05efc8284cb29130efae4bcaefb4834a3fb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917288"
---
# <a name="http-completion-routines"></a>Rotinas de conclusão de HTTP

Os aplicativos têm várias opções para receber indicações de conclusão e fornecer alguma flexibilidade para os desenvolvedores. As opções são bloqueadas enquanto aguardam a conclusão de uma chamada à API ou para usar rotinas de conclusão para operações assíncronas. A vantagem de usar operações assíncronas é um aumento na capacidade de resposta do aplicativo.

## <a name="blocked-io"></a>E/s bloqueada

Os aplicativos podem ser bloqueados enquanto aguardam a conclusão da chamada de API definindo a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) como **NULL**. Isso realmente bloqueia todas as operações no thread. Por exemplo, em chamadas para [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect), a chamada é bloqueada até que a conexão seja interrompida.

## <a name="asynchronous-io"></a>E/s assíncrona

Aplicativos que preferem não bloquear podem usar a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) para obter os resultados de conclusão. O aplicativo fornece um ponteiro para uma estrutura **sobreposta** , que é usada com um objeto de evento ou uma porta de conclusão. Com uma porta de conclusão de e/s, um identificador HTTP é usado como um identificador de arquivo em uma operação de e/s de arquivo assíncrono. A tabela a seguir resume as opções de conclusão disponíveis para os aplicativos.



| Estrutura sobreposta | Objeto de evento   | Porta de conclusão | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | Não Aplicável | Ignored         | A operação é concluída de forma síncrona.                                                                           |
| Não **nulo**         | Não **nulo**   | **NULL**        | A operação é concluída de forma assíncrona. A notificação sobreposta é executada por meio da sinalização de um objeto de evento.       |
| Não **nulo**         | Ignored        | Não **nulo**    | A operação é concluída de forma assíncrona. A notificação sobreposta é executada por meio do agendamento de uma rotina de conclusão. |



 

## <a name="returning-the-number-of-bytes-read"></a>Retornando o número de bytes lidos

Algumas das funções que usam a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) para conclusão assíncrona retornam um parâmetro *PBytesReceived* (ou *pBytesSent* ou *pBytesRead*) que indica o número de bytes transferidos de forma síncrona. Para chamadas assíncronas, esse parâmetro deve ser definido como **nulo**. Para chamadas síncronas, o parâmetro *pBytesReceived* é opcional e pode ser **nulo** ou não **nulo**.

Se o objeto de evento for usado para conclusão assíncrona, a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) será chamada para determinar o número de bytes lidos. Se a porta de conclusão for usada (o parâmetro *hFile* está associado a uma porta de conclusão de e/s), o aplicativo chamará a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para determinar o número de bytes lidos. Se as operações assíncronas não tiverem sido concluídas, os aplicativos poderão chamar a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter informações de erro estendidas.

A tabela a seguir resume o comportamento de conclusão para a conclusão síncrona e assíncrona em funções como [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) que usam o parâmetro *pBytesReceived* .



| pBytesReceived\* | pOverlapped  | Description                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | O aplicativo não recebe informações sobre o número de bytes retornados.           |
| **NULL**         | Não **nulo** | Operação assíncrona, o *pBytesReceived* não faz sentido.                                |
| Não **nulo**     | **NULL**     | Operação síncrona, número de bytes retornados em *pBytesReceived*.                    |
| Não **nulo**     | Não **nulo** | Operação assíncrona, *pBytesReceived* é ignorada, embora não seja **nula**.\*\* |



 

> [!Note]  
> \*Esse parâmetro também pode ser *pBytesSent* ou *pBytesRead*.

 

> [!Note]  
> \*\*É recomendável que os aplicativos passem um **valor nulo** no *pBytesReceived* para operações assíncronas e obtenham o número de bytes recebidos de [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

 

## <a name="return-codes"></a>Códigos de retorno

A API do servidor HTTP retorna três classes de códigos para chamadas de função assíncronas.

-   SEM \_ erros
-   \_e/s de erro \_ pendente
-   Qualquer outro [código de erro do sistema](/windows/desktop/Debug/system-error-codes).

Quando o erro \_ de e/s \_ está pendente ou nenhum \_ erro é retornado da chamada de função assíncrona, os usuários devem esperar que a rotina de evento ou de conclusão seja sinalizada. Chamar a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para o evento ou a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para a porta de conclusão retorna o status de conclusão. Além disso, se nenhum \_ erro for retornado, os aplicativos poderão executar o pós-processamento no mesmo thread que fez a chamada à API.

Se a API do servidor HTTP retornar algo diferente de erro \_ e/s \_ pendente ou nenhum \_ erro, da chamada de função assíncrona, a rotina de conclusão não será sinalizada e o erro será RETORNADO diretamente pela API.

 

 