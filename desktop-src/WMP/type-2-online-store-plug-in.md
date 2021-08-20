---
title: Plug-in da loja online de tipo 2
description: Plug-in da loja online de tipo 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player lojas online, plug-ins
- lojas online, plug-ins
- tipo 2 lojas online, plug-ins
- Windows Media Player online, interface IWMPSubscriptionService
- lojas online, interface IWMPSubscriptionService
- tipo 2 lojas online, interface IWMPSubscriptionService
- plug-ins, Windows Media Player online
- plug-ins, lojas online
- plug-ins, tipo 2 lojas online
- plug-ins, interface IWMPSubscriptionService
- Windows Media Player plug-ins, digite 2 lojas online
- Windows Media Player plug-ins, lojas online
- Windows Media Player plug-ins, Windows Media Player online
- Windows Media Player plug-ins, interface IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254fe0aeed0d03f4437c408f4c00c181fdeb07cf75df8ff9d7a1139ea284150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117473"
---
# <a name="type-2-online-store-plug-in"></a>Plug-in da loja online de tipo 2

Um plug-in de loja online do tipo 2 é um componente COM que implementa a interface [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e, opcionalmente, a interface [IWMPSubscriptionService2.](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) Windows Media Player 9 chama os métodos da interface **IWMPSubscriptionService.** Windows Media Player 10 ou posterior chama os métodos das interfaces **IWMPSubscriptionService** e **IWMPSubscriptionService2.**

Um plug-in de loja online do tipo 2 é empacotado como um servidor COM em processo. Ou seja, o plug-in é implementado em um arquivo .dll que é mapeado para o Windows Media Player processo.

Windows Media Player ativa plug-ins de loja online do tipo 2 conforme necessário. Por exemplo, suponha que o usuário tenta tocar uma música protegida e não há nenhuma licença atual para reproduzi-la. Nesse caso, Windows Media Player inspecione o atributo **ContentDistributor** no título do arquivo ou no header drm. Se existir um valor que corresponde ao nome da chave de um armazenamento online, o Windows Media Player verificará o Registro para ver se a loja online forneceu um plug-in do tipo 2. Se o plug-in existir, Windows Media Player carregará o plug-in e chamará seus métodos para determinar se o usuário tem os direitos de tocar a música.

A lista a seguir descreve alguns dos cenários em que o Windows Media Player chama um plug-in de loja online do tipo 2.

-   **O usuário tenta reproduzir o conteúdo da loja online.** Quando isso acontece, Windows Media Player chama o método [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) do plug-in, passando um ponteiro para o item de mídia digital que o usuário está tentando reproduzir. A loja online pode usar isso como uma oportunidade para atualizar a licença do usuário para reproduzir o conteúdo ou para não permitir a reprodução. Se o plug-in retornar **TRUE** no *parâmetro pfAllowPlay,* Windows Media Player tentará reproduzir o conteúdo. A reprodução ainda falhará se uma licença válida não existir; esse processo não contorna o DRM (gerenciamento de direitos digitais).
-   **O usuário solicita permissão para gravar conteúdo em um CD ou DVD.** Quando isso acontece, Windows Media Player chama o método [IWMPSubscriptionService::allowCDScript do](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) plug-in.
-   **O usuário tenta sincronizar o conteúdo da loja online com um dispositivo ou Windows Media Player está pronto para sincronizar automaticamente o conteúdo da loja online com um dispositivo.** Quando isso acontece, o Windows Media Player chama o método [IWMPSubscriptionService2::p repareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) do plug-in para alertar o armazenamento online de que um item de mídia está prestes a ser sincronizado com um dispositivo específico, que é identificado pelo nome canônico. Essa é uma oportunidade para a loja online determinar se o usuário tem permissão para sincronizar o item de mídia com o dispositivo. Também é uma oportunidade para a loja online preparar o dispositivo para sincronização e atualizar registros, como contagens de sincronização, associadas ao dispositivo ou ao item de mídia. O plug-in deve passar as tarefas de permissão, preparação e manutenção de registro para um thread separado e retornar imediatamente **de prepareForSync.** Quando o thread separado terminar seu trabalho, ele deverá notificar Windows Media Player chamando [IWMPSubscriptionServiceCallback::onComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Um dispositivo fica disponível para processamento em segundo plano.** Quando um dispositivo está conectado, Windows Media Player alerta o armazenamento online de que o dispositivo está disponível e ocioso chamando [IWMPSubscriptionService2::d eviceAvailable.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)
-   **O usuário clica em um botão para ativar uma loja online no Windows Media Player.** Quando isso ocorre, Windows Media Player chama o método [IWMPSubscriptionService2::serviceEvent do](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) plug-in. Windows Media Player também chama esse método quando o usuário alterna para outro serviço.
-   **Windows Media Player entra em um estado de baixa atividade.** Quando isso acontece, o Player chama o método [IWMPSubscriptionService::startBackgroundProcessing do](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) plug-in. O armazenamento online pode usar essa oportunidade para iniciar ou ativas threads que executam tarefas em segundo plano, como renovar licenças expiradas ou compilar dados de contagem de reprodução.
-   **Windows Media Player entra em um estado de alta atividade.** Quando isso acontece, Windows Media Player chama o método [IWMPSubscriptionService2::stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) do plug-in. Isso informa ao plug-in que ele deve suspender todos os threads que estão executando tarefas em segundo plano.

Windows Media Player libera o componente da loja online quando a sessão do Player termina. Após o lançamento, o componente deve interromper qualquer processamento em segundo plano em andamento e, em seguida, desligar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPSubscriptionService Interface**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2 Interface**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**IWMPSubscriptionServiceCallback Interface**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Exemplos da Loja Online do Tipo 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




