---
description: todos os processos (aplicativos ou DLLs) que chamam funções winsock devem inicializar o uso da DLL de soquetes de Windows antes de fazer outras chamadas de funções do Winsock. Isso também faz com que o Winsock tenha suporte no sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inicializando o Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aad1dc5bffb09490a963bd86c61c6cc2a857fec45251b38111ab790db8a26e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051514"
---
# <a name="initializing-winsock"></a>Inicializando o Winsock

todos os processos (aplicativos ou DLLs) que chamam funções winsock devem inicializar o uso da DLL de soquetes de Windows antes de fazer outras chamadas de funções do Winsock. Isso também faz com que o Winsock tenha suporte no sistema.

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

a estrutura [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contém informações sobre a implementação de soquetes de Windows. o parâmetro MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) faz uma solicitação para a versão 2,2 do Winsock no sistema e define a versão passada como a versão mais recente do suporte a soquetes de Windows que o chamador pode usar.

Próxima etapa para um cliente: [criando um soquete para o cliente](creating-a-socket-for-the-client.md)

Próxima etapa para um servidor: [criando um soquete para o servidor](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Criando um aplicativo Winsock básico](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



