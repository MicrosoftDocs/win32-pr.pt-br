---
title: Plug-in da loja online de tipo 2
description: Plug-in da loja online de tipo 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 2 lojas online, plug-ins
- Lojas online do Windows Media Player, interface IWMPSubscriptionService
- lojas online, interface IWMPSubscriptionService
- tipo 2 lojas online, interface IWMPSubscriptionService
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, tipo 2 lojas online
- plug-ins, interface IWMPSubscriptionService
- Plug-ins do Windows Media Player, tipo 2 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, interface IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d2f3aeeaa7456c3452b498a1a728e24c96783c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084401"
---
# <a name="type-2-online-store-plug-in"></a>Plug-in da loja online de tipo 2

Um plug-in de loja online tipo 2 é um componente COM que implementa a interface [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e, opcionalmente, a interface [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) . O Windows Media Player 9 chama os métodos da interface **IWMPSubscriptionService** . O Windows Media Player 10 ou posterior chama os métodos das interfaces **IWMPSubscriptionService** e **IWMPSubscriptionService2** .

Um plug-in de loja online tipo 2 é empacotado como um servidor COM em processo. Ou seja, o plug-in é implementado em um arquivo. dll que é mapeado para o processo do Windows Media Player.

O Windows Media Player ativa plug-ins de loja online do tipo 2, conforme necessário. Por exemplo, suponha que o usuário tente reproduzir uma música protegida e não haja licença atual para reproduzi-la. Nesse caso, o Windows Media Player inspeciona o atributo **ContentDistributor** no cabeçalho do arquivo ou no cabeçalho DRM. Se existir um valor que corresponda ao nome da chave de uma loja online, o Windows Media Player verificará o registro para ver se o repositório online forneceu um plug-in do tipo 2. Se o plug-in existir, o Windows Media Player carregará o plug-in e chamará seus métodos para determinar se o usuário tem os direitos de reproduzir a música.

A lista a seguir descreve alguns dos cenários nos quais o Windows Media Player chama um plug-in de loja online tipo 2.

-   **O usuário tenta reproduzir o conteúdo da loja online.** Quando isso acontece, o Windows Media Player chama o método [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) do plug-in, passando um ponteiro para o item de mídia digital que o usuário está tentando reproduzir. O repositório online pode usar isso como uma oportunidade de atualizar a licença do usuário para reproduzir o conteúdo ou para não permitir a reprodução. Se o plug-in retornar **true** no parâmetro *PfAllowPlay* , o Windows Media Player tentará reproduzir o conteúdo. A reprodução continuará falhando se uma licença válida não existir; Esse processo não evita o gerenciamento de direitos digitais (DRM).
-   **O usuário solicita permissão para gravar conteúdo em um CD ou DVD.** Quando isso acontece, o Windows Media Player chama o método [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) do plug-in.
-   **O usuário tenta sincronizar o conteúdo da loja online com um dispositivo ou o Windows Media Player está pronto para sincronizar automaticamente o conteúdo da loja online com um dispositivo.** Quando isso acontece, o Windows Media Player chama o método [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) do plug-in para alertar a loja online que um item de mídia está prestes a ser sincronizado com um dispositivo específico, que é identificado por seu nome canônico. Essa é uma oportunidade para a loja online determinar se o usuário tem permissão para sincronizar o item de mídia com o dispositivo. Também é uma oportunidade para a loja online preparar o dispositivo para sincronização e para atualizar registros, como contagens de sincronização, associadas ao dispositivo ou ao item de mídia. O plug-in deve passar as tarefas de permissão, preparação e manutenção de registros para um thread separado e retornar imediatamente do **prepareForSync**. Quando o thread separado terminar seu trabalho, ele deverá notificar o Windows Media Player chamando [IWMPSubscriptionServiceCallback:: OnComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Um dispositivo fica disponível para processamento em segundo plano.** Quando um dispositivo está conectado, o Windows Media Player alerta a loja online de que o dispositivo está disponível e está ocioso chamando [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **O usuário clica em um botão para ativar uma loja online no Windows Media Player.** Quando isso ocorre, o Windows Media Player chama o método [IWMPSubscriptionService2:: OnEvent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) do plug-in. O Windows Media Player também chama esse método quando o usuário alterna para outro serviço.
-   **O Windows Media Player entra em um estado de baixa atividade.** Quando isso acontece, o Player chama o método [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) do plug-in. O repositório online pode usar essa oportunidade para iniciar ou ativar quaisquer threads que executam tarefas em segundo plano, como renovar licenças expiradas ou compilar dados de contagem de reprodução.
-   **O Windows Media Player entra em um estado de alta atividade.** Quando isso acontece, o Windows Media Player chama o método [IWMPSubscriptionService2:: stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) do plug-in. Isso informa ao plug-in que ele deve suspender os threads que estão executando tarefas em segundo plano.

O Windows Media Player libera o componente de loja online quando a sessão do Player termina. Após a liberação, o componente deve interromper qualquer processamento em segundo plano em andamento e, em seguida, desligar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interface IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**Interface IWMPSubscriptionServiceCallback**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Tipo 2 amostras de loja online**](type-2-online-store-samples.md)
</dt> </dl>

 

 




