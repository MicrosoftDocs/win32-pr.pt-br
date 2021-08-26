---
title: Como funciona o RPC
description: As ferramentas de RPC fazem parecer aos usuários como se um cliente chama diretamente um procedimento localizado em um programa de servidor remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd7a3adf59e848d962d4765a0feee16eb1fa84842c2a1ddd34ed82ecf95a8e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020846"
---
# <a name="how-rpc-works"></a>Como funciona o RPC

As ferramentas de RPC fazem parecer aos usuários como se um cliente chama diretamente um procedimento localizado em um programa de servidor remoto. Cada cliente e servidor têm seus próprios espaços de endereço; ou seja, cada um tem seu próprio recurso de memória alocado aos dados usados pelo procedimento. A figura a seguir ilustra a arquitetura RPC.

![arquitetura rpc](images/prog-a11.png)

Como mostra a ilustração, o aplicativo cliente chama um procedimento de stub local em vez do código real que implementa o procedimento. Os stubs são compilados e vinculados ao aplicativo cliente. Em vez de conter o código real que implementa o procedimento remoto, o código de stub do cliente:

-   Recupera os parâmetros necessários do espaço de endereço do cliente.
-   Converte os parâmetros conforme necessário em um formato NDR padrão para transmissão pela rede.
-   Chama funções na biblioteca de tempo de run time do cliente RPC para enviar a solicitação e seus parâmetros para o servidor.

O servidor executa as etapas a seguir para chamar o procedimento remoto.

1.  As funções de biblioteca em tempo de executar RPC do servidor aceitam a solicitação e chamam o procedimento de stub do servidor.
2.  O stub do servidor recupera os parâmetros do buffer de rede e os converte do formato de transmissão de rede para o formato de que o servidor precisa.
3.  O stub do servidor chama o procedimento real no servidor.

Em seguida, o procedimento remoto é executado, possivelmente gerando parâmetros de saída e um valor de retorno. Quando o procedimento remoto é concluído, uma sequência semelhante de etapas retorna os dados para o cliente.

1.  O procedimento remoto retorna seus dados para o stub do servidor.
2.  O stub do servidor converte parâmetros de saída no formato necessário para transmissão pela rede e os retorna para as funções de biblioteca em tempo de run-time RPC.
3.  As funções de biblioteca em tempo de executar RPC do servidor transmitem os dados na rede para o computador cliente.

O cliente conclui o processo aceitando os dados pela rede e retornando-os para a função de chamada.

1.  A biblioteca de tempo de executar RPC do cliente recebe os valores de retorno de procedimento remoto e os retorna para o stub do cliente.
2.  O stub do cliente converte os dados de sua NDR no formato usado pelo computador cliente. O stub grava dados na memória do cliente e retorna o resultado para o programa de chamada no cliente.
3.  O procedimento de chamada continua como se o procedimento tivesse sido chamado no mesmo computador.

As bibliotecas em tempo de execução são fornecidas em duas partes: uma biblioteca de importação, que está vinculada ao aplicativo e à biblioteca em tempo de execução RPC, que é implementada como uma DLL (biblioteca de vínculo dinâmico).

O aplicativo de servidor contém chamadas para as funções de biblioteca em tempo de executar servidor que registram a interface do servidor e permitem que o servidor aceite chamadas de procedimento remoto. O aplicativo de servidor também contém os procedimentos remotos específicos do aplicativo que são chamados pelos aplicativos cliente.

 

 




