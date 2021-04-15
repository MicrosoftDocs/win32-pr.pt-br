---
description: Todos os processos (aplicativos ou DLLs) que chamam funções Winsock devem inicializar o uso da DLL do Windows Sockets antes de fazer outras chamadas de funções do Winsock. Isso também faz com que o Winsock tenha suporte no sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inicializando o Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501691"
---
# <a name="initializing-winsock"></a>Inicializando o Winsock

Todos os processos (aplicativos ou DLLs) que chamam funções Winsock devem inicializar o uso da DLL do Windows Sockets antes de fazer outras chamadas de funções do Winsock. Isso também faz com que o Winsock tenha suporte no sistema.

**Para inicializar o Winsock**

1.  Crie um objeto [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) chamado WSADATA.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Chame [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) e retorne seu valor como um inteiro e verifique se há erros.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

A função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) é chamada para iniciar o uso de ws2 \_32.dll.

A estrutura [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contém informações sobre a implementação do Windows Sockets. O parâmetro MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) faz uma solicitação para a versão 2,2 do Winsock no sistema e define a versão passada como a versão mais recente do suporte do Windows Sockets que o chamador pode usar.

Próxima etapa para um cliente: [criando um soquete para o cliente](creating-a-socket-for-the-client.md)

Próxima etapa para um servidor: [criando um soquete para o servidor](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Criando um aplicativo Winsock básico](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



