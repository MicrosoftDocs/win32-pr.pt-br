---
title: Desenvolvimento de cliente usando identificadores de contexto
description: O único uso de um programa cliente para um identificador de contexto é passá-lo para o servidor sempre que o cliente fizer uma chamada de procedimento remoto.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498775"
---
# <a name="client-development-using-context-handles"></a>Desenvolvimento de cliente usando identificadores de contexto

O único uso de um programa cliente para um identificador de contexto é passá-lo para o servidor sempre que o cliente fizer uma chamada de procedimento remoto. O aplicativo cliente não precisa acessar o conteúdo do identificador. Ele não deve tentar alterar os dados de identificador de contexto de forma alguma. Os procedimentos remotos que o cliente invoca executam todas as operações necessárias no contexto do servidor.

Antes de solicitar um identificador de contexto de um servidor, os clientes devem estabelecer uma ligação com o servidor. O cliente pode usar um identificador de associação automático, implícito ou explícito. Com um identificador de associação válido, o cliente pode chamar um procedimento remoto no servidor que retorna um identificador de contexto aberto (não **nulo**) ou passa um por um parâmetro de **\[ saída \]** na lista de parâmetros do procedimento remoto.

Os clientes podem usar identificadores de contexto abertos de qualquer maneira que exijam. No entanto, eles devem invalidar o identificador quando eles não precisarem mais dele. Há duas maneiras de fazer isso:

-   Para invocar um procedimento remoto oferecido pelo programa de servidor que libera o contexto e fecha o identificador de contexto (define-o como **nulo**).
-   Quando o servidor estiver inacessível, chame a função [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .

A segunda abordagem limpa apenas o estado do lado do cliente e não limpa o estado do lado do servidor, portanto, ele deve ser usado somente quando a partição de rede for suspeita e o cliente e o servidor farão uma limpeza independente. O servidor executa a limpeza independente por meio da rotina de execução, o cliente faz isso usando a função [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .

O fragmento de código a seguir apresenta um exemplo de como um cliente pode usar um identificador de contexto. Para exibir a definição da interface que este exemplo usa, consulte [desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md). Para a implementação do servidor, consulte [desenvolvimento de servidor usando identificadores de contexto](server-development-using-context-handles.md).

Neste exemplo, o cliente chama RemoteOpen para obter um identificador de contexto que contém dados válidos. O cliente pode usar o identificador de contexto em chamadas de procedimento remoto. Como ele não precisa mais do identificador de associação, o cliente pode liberar o identificador explícito usado para criar o identificador de contexto:


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



O aplicativo cliente neste exemplo usa um procedimento chamado RemoteRead para ler um arquivo de dados no servidor até encontrar um final de arquivo. Em seguida, ele fecha o arquivo chamando RemoteClose. O identificador de contexto aparece como um parâmetro nas funções RemoteRead e RemoteClose como:


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




