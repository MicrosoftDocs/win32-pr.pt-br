---
title: Desenvolvimento de cliente usando alças de contexto
description: O único uso que um programa cliente tem para um handle de contexto é passá-lo para o servidor sempre que o cliente fizer uma chamada de procedimento remoto.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ff599bebdf042bc2021d53538cff1c0203d2de875bdc52c50a72675b73a47f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931837"
---
# <a name="client-development-using-context-handles"></a>Desenvolvimento de cliente usando alças de contexto

O único uso que um programa cliente tem para um handle de contexto é passá-lo para o servidor sempre que o cliente fizer uma chamada de procedimento remoto. O aplicativo cliente não precisa acessar o conteúdo do handle. Ele não deve tentar alterar os dados do lidar com o contexto de nenhuma maneira. Os procedimentos remotos que o cliente invoca executam todas as operações necessárias no contexto do servidor.

Antes de solicitar um handle de contexto de um servidor, os clientes devem estabelecer uma associação com o servidor. O cliente pode usar um alça de associação automática, implícita ou explícita. Com um alça de associação válido, o cliente pode chamar um procedimento remoto no servidor que **\[ \]** retorna um alça de contexto aberto (não **NULL)** ou passa um por meio de um parâmetro out na lista de parâmetros do procedimento remoto.

Os clientes podem usar os alças de contexto abertos da maneira que eles exigirem. No entanto, eles devem invalidar o alça quando não precisam mais dele. Há duas maneira de fazer isso:

-   Para invocar um procedimento remoto oferecido pelo programa de servidor que libera o contexto e fecha o handle de contexto (define-o como **NULL).**
-   Quando o servidor estiver inacessível, chame a [**função RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

A segunda abordagem limpa apenas o estado do lado do cliente e não limpa o estado do lado do servidor, portanto, ela deve ser usada somente quando há suspeita de partição de rede e o cliente e o servidor fará uma limpeza independente. O servidor executa a limpeza independente por meio da rotina de execução, o cliente faz isso usando a [**função RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

O fragmento de código a seguir apresenta um exemplo de como um cliente pode usar um handle de contexto. Para exibir a definição da interface que este exemplo usa, consulte [Desenvolvimento de interface usando alças de contexto](interface-development-using-context-handles.md). Para a implementação do servidor, consulte [Desenvolvimento de servidor usando alças de contexto](server-development-using-context-handles.md).

Neste exemplo, o cliente chama RemoteOpen para obter um handle de contexto que contém dados válidos. Em seguida, o cliente pode usar o alça de contexto em chamadas de procedimento remoto. Como ele não precisa mais do alça de associação, o cliente pode liberar o handle explícito usado para criar o alça de contexto:


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



O aplicativo cliente neste exemplo usa um procedimento chamado RemoteRead para ler um arquivo de dados no servidor até encontrar um fim do arquivo. Em seguida, ele fecha o arquivo chamando RemoteClose. O alça de contexto aparece como um parâmetro nas funções RemoteRead e RemoteClose como:


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



 

 




