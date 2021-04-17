---
description: Uma operação que é concluída de forma assíncrona realiza parte de seu processamento na chamada de função feita pelo aplicativo e o restante dele em um thread de execução independente após a TAPI 2. x ter retornado da chamada de função.
ms.assetid: 37b544e4-6413-4741-b8b6-ec676ce4ca97
title: Funções assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e792a4b1d6a25a4f49fbb2abe2c19ce3071ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754202"
---
# <a name="asynchronous-functions"></a>Funções assíncronas

Uma operação que é concluída de forma assíncrona realiza parte de seu processamento na chamada de função feita pelo aplicativo e o restante dele em um thread de execução independente após a TAPI 2. x ter retornado da chamada de função. Para garantir a conclusão do processamento da chamada, o provedor de serviços faz o vetor da solicitação para outra entidade ativa no sistema — como um servidor de LAN, um hardware de suplemento, um comutador ou uma rede — e, em seguida, retorna ao aplicativo. Neste momento, um resultado de erro negativo ou um identificador de solicitação positivo é retornado para o aplicativo.

No momento da conclusão assíncrona (o provedor de serviços recebeu uma interrupção do hardware, o que significa que uma mensagem deve ser entregue), o provedor de serviços chama TAPISRV e relata que "evento *X* acabou de acontecer. Forneça uma mensagem apropriada para todos os aplicativos preocupados. " Quando o TAPISRV recebe essa mensagem, ele encaminha a mensagem para a biblioteca de vínculo dinâmico TAPI, no processo do aplicativo, que, por sua vez, posta uma mensagem de janela, sinaliza um identificador de evento ou posta em uma porta de conclusão de e/s, de acordo com o esquema de notificação de mensagem selecionado pelo aplicativo em [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) ou [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa).

Quando a parte assíncrona da operação é concluída, uma mensagem de [**\_ resposta de linha**](./line-reply.md) (ou [**\_ resposta telefônica**](./phone-reply.md)) é enviada para o aplicativo. Essa mensagem contém, como um de seus parâmetros, o identificador da solicitação retornado pela chamada de função. Esse identificador de solicitação permite que o aplicativo determine qual solicitação original foi concluída. (Os aplicativos devem lembrar os identificadores de solicitação de todas as suas solicitações em andamento para que as mensagens de resposta possam ser manipuladas adequadamente.) Um segundo parâmetro para a mensagem de resposta de linha \_ (ou \_ resposta telefônica) é o valor de retorno assíncrono. Esse é um valor negativo (para um erro) ou zero se a operação foi concluída com êxito. Para operações assíncronas, qualquer um dos valores de retorno pode ser retornado como parte do retorno da função ou como o parâmetro *dwParam2* na \_ mensagem de resposta do telefone ou resposta de linha \_ . O valor 0, que indica êxito, será retornado apenas na mensagem de resposta de linha \_ e nunca como o valor de retorno da função.

As funções de inicialização ( [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) e [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)) dizem ao TAPI como enviar essas mensagens para o aplicativo.

> [!Note]  
> Em alguns casos, se um aplicativo multi-threaded chamar uma função assíncrona de um thread que não seja o thread do qual o aplicativo inicializou a linha ou o dispositivo de telefone, o aplicativo poderá receber a [**\_ resposta de linha**](./line-reply.md) ou a mensagem de [**\_ resposta do telefone**](./phone-reply.md) antes que a função assíncrona seja retornada. Nesses casos, o aplicativo deve salvar os parâmetros da mensagem e aguardar até que a função assíncrona seja retornada e o identificador da solicitação seja conhecido antes de processar a mensagem.

 

 

 
