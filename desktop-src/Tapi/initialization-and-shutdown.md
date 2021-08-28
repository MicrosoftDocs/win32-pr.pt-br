---
description: Para que um aplicativo use qualquer uma das TAPIs 30 funções de telefone suplementares, ele precisa de uma conexão com a TAPI, por meio da qual ele pode receber mensagens.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Inicialização e desligamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7414b78636a7ce7bf93e297b0cbef4d9dc7d6482191c1b1948235d1dc117423
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867286"
---
# <a name="initialization-and-shutdown"></a>Inicialização e desligamento

Para que um aplicativo use qualquer uma das 30 funções de telefone complementares da TAPI, ele precisa de uma conexão com a TAPI, por meio da qual ele pode receber mensagens. O aplicativo estabelece essa conexão usando a função [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) . Nessa função, o aplicativo especifica o mecanismo de notificação pelo qual a TAPI informa a aplicação das alterações no estado do telefone e da conclusão assíncrona de funções de telefone.

A função [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) retorna duas partes de informações para o aplicativo: um *identificador de aplicativo* e o número de dispositivos de telefone. O identificador do aplicativo representa o uso do aplicativo TAPI. As funções TAPI que usam identificadores de telefone não exigem o identificador do aplicativo, pois esse identificador é derivado do identificador de telefone especificado.

A segunda informação retornada por [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) é o número de dispositivos de telefone disponíveis para a TAPI. Telefone dispositivos são identificados pelo seu identificador de dispositivo (*ID do dispositivo*). Os identificadores de dispositivo válidos variam de zero até o número de dispositivos de telefone menos um. Por exemplo, se **phoneInitializeEx** relata que há dois dispositivos telefônicos em um sistema, os identificadores de dispositivo de telefone válidos são 0 e 1. Depois que um aplicativo é concluído usando as funções de telefone da TAPI, ele invoca o [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown), passando seu identificador de aplicativo para desligar o uso da TAPI. Isso permite que a TAPI libere todos os recursos atribuídos ao aplicativo.

Os aplicativos não devem invocar [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) sem abrir um telefone subsequentemente (pelo menos para monitoramento). Se o aplicativo não estiver monitorando e não estiver usando nenhum dispositivo, ele deverá chamar [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) para que os recursos de memória alocados pela biblioteca de vínculo dinâmico TAPI possam ser liberados, se desnecessário, e a própria biblioteca possa ser descarregada da memória, embora não seja necessário.

[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) e [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) operam de forma síncrona. Ou seja, essas funções retornam uma indicação de êxito ou falha e nunca retornam um identificador de solicitação assíncrono.

 

 



