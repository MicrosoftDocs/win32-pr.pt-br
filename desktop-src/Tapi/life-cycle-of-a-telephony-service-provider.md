---
description: Este tópico fornece uma revisão de alto nível das operações de TSP.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Ciclo de vida de um provedor de serviços de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6282f4e7b946ffb79bd6233688869616cc0b0259a1d491834452290474c552a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012688"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Ciclo de vida de um provedor de serviços de telefonia

Este tópico fornece uma revisão de alto nível das operações de TSP.

Uma sessão é o tempo durante o qual uma configuração específica permanece válida e as operações de telefonia são executadas. Um provedor de serviços pode dar suporte a várias sessões entre o momento em que é carregado pela primeira vez e quando é finalmente liberado. Para cada sessão, a TAPI negocia a versão da interface, inicia a sessão, executa operações e, eventualmente, desliga a sessão. O provedor de serviços não deve reter informações de uma sessão para a próxima.

Depois que a versão da interface é conhecida, a TAPI chama a função [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) para definir todos os parâmetros operacionais. O provedor de serviços garante que todas as informações de configuração no registro sejam estáveis quando a função **TSPI \_ providerInit** for chamada. A maioria dos provedores de serviços lê todas as informações de configuração nesse momento.

As operações normais podem continuar em qualquer ordem, depois que o provedor de serviços for inicializado.

A TAPI negocia informações específicas do dispositivo em uma base por dispositivo. A TAPI e o provedor de serviços são confirmados em uma versão quando um dispositivo é aberto.

O provedor de serviços pode receber solicitações para selecionar e cancelar versões de extensão. Enquanto uma versão de extensão é selecionada, o dispositivo opera estritamente de acordo com essa versão de extensão específica do dispositivo.

A negociação de uma versão de extensão específica do dispositivo pode ocorrer várias vezes, antes e depois que o dispositivo é aberto. A TAPI passa um intervalo de versão e o provedor de serviço escolhe e retorna um valor desse intervalo. Normalmente, o provedor de serviços tem extensões específicas do dispositivo desabilitadas.

Isso confirma a TAPI e o provedor de serviços para operar nesse nível de versão de extensão até que a seleção seja cancelada. Durante o tempo em que uma extensão específica do dispositivo está em vigor, uma tentativa de negociar um nível de versão de extensão deve permitir apenas o nível de versão atualmente em vigor. Depois que a extensão específica do dispositivo for cancelada, uma versão diferente poderá ser negociada e selecionada.

Telefone operações dentro do par **abrir/fechar** são mostradas na ilustração a seguir. Algumas dessas operações são síncronas, outras são assíncronas. Se uma operação for concluída de forma assíncrona, outra operação poderá ser solicitada antes da conclusão da primeira relatórios. Portanto, as operações podem se sobrepor de qualquer forma. O provedor de serviços deve eventualmente relatar a conclusão para qualquer operação assíncrona solicitada. Fechar um telefone força a conclusão de operações assíncronas pendentes (possivelmente com uma indicação de "falha").

O ciclo de vida para dispositivos de linha é semelhante ao ciclo de vida de telefones, exceto que as linhas têm seus próprios procedimentos de negociação, inicialização, abertura e fechamento. As operações em linhas abertas estão entredas por seu próprio par de **abertura/fechamento** . Esse par é, por sua vez, emparelhado entre o mesmo par de **inicialização/desligamento** que o telefone **abre/fecha**.

Os ciclos de vida de chamadas são dealinhados estritamente entre o **abrir/fechar** da linha que os contém. Os tempos de vida das chamadas podem começar de várias maneiras:

-   Solicitado da TAPI por meio de funções como [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)ou [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference).
-   Espontaneamente originado no provedor de serviços como novas chamadas de entrada, chamadas iniciadas pelo usuário em um aparelho telefônico conectado ou chamadas geradas como um efeito colateral de outras operações, como colocar uma chamada existente em espera.

Os tempos de vida de chamadas distintas dentro da mesma linha podem se sobrepor de qualquer forma. Todas as chamadas encerram seu tempo de vida no momento em que a função TSPI [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) é invocada. O ciclo de vida de várias chamadas é mostrado na ilustração a seguir.

![ciclos de vida de chamadas sobrepostas](images/modell.png)

Uma chamada pode se originar na TAPI, conforme mostrado com o par **MakeCall/CloseCall** . Uma chamada também pode ser originada no provedor de serviços. O provedor de serviços anuncia isso com uma [**mensagem \_ NewCall de linha**](line-newcall.md) para um procedimento de retorno de chamada fornecido pela TAPI. Nesse caso, a TAPI retorna seu identificador para a chamada, que está incluído nos retornos de chamada subsequentes relatando eventos que ocorrem na chamada. No caso de chamadas cujo tempo de vida se origina na TAPI, esse identificador é incluído na operação TSPI que cria a chamada.

Todas as operações que iniciam o tempo de vida de uma chamada resultam na TAPI e no provedor de serviços que trocam identificadores para a nova chamada. No caso de chamadas originadas pela TAPI, a TAPI passa seu identificador e recebe o identificador do provedor de serviços como um parâmetro de retorno. No caso em que a chamada se origina no provedor de serviços, o provedor de serviços passa seu identificador para TAPI e recebe o identificador TAPI como um parâmetro de retorno.

A ilustração a seguir oferece uma exibição de alto nível da instalação, configuração e remoção do provedor de serviços; sequências do ciclo de vida que abrangem muitas sessões. O ciclo de vida típico dessas operações pode ser mostrado com a seguinte linha de tempo.

![instalação, configuração e remoção do provedor de serviços](images/model2.png)

O ciclo de vida de instalação e remoção típico é mostrado, abrangendo várias sessões. As chamadas para os procedimentos **instalar** e [**remover**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) são estritamente emparelhadas e não se sobrepõem. As chamadas para o procedimento de **configuração** podem ocorrer várias vezes neste par. Normalmente, é feito pelo provedor de serviços como um efeito colateral interno do procedimento de **instalação** para criar entradas de linha e telefone. O procedimento de **configuração** pode ser chamado em outras ocasiões para alterar uma configuração existente. O procedimento de **instalação** deve ser feito antes que qualquer outra função TSPI seja permitida. No cenário ideal, todas as sessões são estritamente aninhadas no par de procedimentos de **instalação/remoção** .

As funções [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)e [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interagem com o próprio provedor de serviços em vez de com qualquer dispositivo específico. Eles afetam as informações de configuração estática que sobrevivem em várias sessões e devem estar presentes para que qualquer outra operação continue. Assim, todas as outras operações são aninhadas entre a invocação de **TSPI \_ providerInstall** e a conclusão de **sua \_ providerRemove de TSPI** correspondente. Essas duas operações normalmente ocorrem muito distantes, provavelmente em uma carga diferente do provedor de serviços ou uma inicialização diferente da máquina. Chamar a função de **configuração** externamente é opcional, pois o procedimento de **instalação** é necessário para incluir o comportamento de **configuração** além de seu próprio. O motivo comum para chamá-lo externamente é modificar uma configuração existente.

Há uma sutileza incorporada no conceito da conclusão de uma operação [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) . É desejável permitir que o usuário execute o utilitário do painel de controle de telefonia fornecido com o serviço de telefonia para alterar as configurações do provedor de serviços, mesmo quando as operações de telefonia (sessões) estiverem em andamento. Consequentemente, as especificações [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) e **TSPI \_ providerRemove** permitem a invocação enquanto houver uma sessão pendente. No entanto, as alterações na configuração devem ser atrasadas até que as operações de telefonia sejam desligadas e reiniciadas. Portanto, estritamente falando, a conclusão de qualquer operação **TSPI \_ providerConfig** ou **TSPI \_ providerRemove** acontece fora de qualquer sessão. O aninhamento de ações é como mostrado na figura, embora as chamadas de procedimentos possam aparecer em uma ordem ligeiramente diferente. É permitido para um provedor de serviços simplesmente não permitir a **configuração** ou [**remover**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) enquanto as operações estão em andamento, embora o usuário deva ser notificado com uma caixa de diálogo. Uma implementação mais amigável que permite pelo menos um subconjunto de operações é preferencial.

Essas operações de **instalação**, **configuração** e [**remoção**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) têm o efeito colateral de sinalizar qualquer aplicativo de telefonia em execução, o que eventualmente resulta no desligamento do uso do serviço de telefonia. Juntos, isso encerra todas as sessões pendentes para provedores de serviço. Isso significa aos provedores de serviços que eles devem ler a nova configuração do registro quando novas sessões começam. As alterações que estavam pendentes devido a uma **configuração** ou [**remoção**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) enquanto as operações estavam em andamento entram em vigor.

 

 
