---
title: Como funciona o RPC
description: As ferramentas de RPC o tornam aparentemente para os usuários como se um cliente chama diretamente um procedimento localizado em um programa de servidor remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636346"
---
# <a name="how-rpc-works"></a>Como funciona o RPC

As ferramentas de RPC o tornam aparentemente para os usuários como se um cliente chama diretamente um procedimento localizado em um programa de servidor remoto. O cliente e o servidor têm seus próprios espaços de endereço; ou seja, cada um tem seu próprio recurso de memória alocado aos dados usados pelo procedimento. A figura a seguir ilustra a arquitetura RPC.

![arquitetura de RPC](images/prog-a11.png)

Como mostra a ilustração, o aplicativo cliente chama um procedimento de stub local em vez do código real que implementa o procedimento. Os stubs são compilados e vinculados com o aplicativo cliente. Em vez de conter o código real que implementa o procedimento remoto, o código stub do cliente:

-   Recupera os parâmetros necessários do espaço de endereço do cliente.
-   Traduz os parâmetros conforme necessário em um formato NDR padrão para transmissão pela rede.
-   Chama funções na biblioteca de tempo de execução do cliente RPC para enviar a solicitação e seus parâmetros para o servidor.

O servidor executa as etapas a seguir para chamar o procedimento remoto.

1.  As funções de biblioteca de tempo de execução RPC do servidor aceitam a solicitação e chamam o procedimento de stub do servidor.
2.  O stub do servidor recupera os parâmetros do buffer de rede e os converte do formato de transmissão de rede para o formato que o servidor precisa.
3.  O stub de servidor chama o procedimento real no servidor.

Em seguida, o procedimento remoto é executado, possivelmente gerando parâmetros de saída e um valor de retorno. Quando o procedimento remoto é concluído, uma sequência semelhante de etapas retorna os dados para o cliente.

1.  O procedimento remoto retorna seus dados para o stub do servidor.
2.  O stub de servidor converte parâmetros de saída para o formato necessário para transmissão pela rede e os retorna para as funções de biblioteca de tempo de execução RPC.
3.  As funções de biblioteca de tempo de execução RPC do servidor transmitem os dados na rede para o computador cliente.

O cliente conclui o processo aceitando os dados pela rede e retornando-os para a função de chamada.

1.  A biblioteca de tempo de execução RPC do cliente recebe os valores de retorno de procedimento remoto e os retorna ao stub do cliente.
2.  O stub do cliente converte os dados de seu NDR para o formato usado pelo computador cliente. O stub grava dados na memória do cliente e retorna o resultado para o programa de chamada no cliente.
3.  O procedimento de chamada continua como se o procedimento tivesse sido chamado no mesmo computador.

As bibliotecas de tempo de execução são fornecidas em duas partes: uma biblioteca de importação, que é vinculada ao aplicativo e à biblioteca de tempo de execução RPC, que é implementada como uma DLL (biblioteca de vínculo dinâmico).

O aplicativo de servidor contém chamadas para as funções de biblioteca de tempo de execução do servidor que registram a interface do servidor e permitem que o servidor aceite chamadas de procedimento remotas. O aplicativo de servidor também contém os procedimentos remotos específicos do aplicativo que são chamados pelos aplicativos cliente.

 

 




