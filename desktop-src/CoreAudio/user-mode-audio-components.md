---
description: User-Mode componentes de áudio
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode componentes de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18715db2d32be3c4a70182571028acbfca411539
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826476"
---
# <a name="user-mode-audio-components"></a>User-Mode componentes de áudio

No Windows Vista, as APIs de áudio principais servem como a base do subsistema de áudio do modo de usuário. As principais APIs de áudio são implementadas como uma camada fina de componentes do sistema de modo de usuário que separam clientes de modo de usuário de drivers de áudio no modo kernel e hardware de áudio. As APIs de áudio de nível superior, como DirectSound e as funções de multimídia do Windows, acessam dispositivos de áudio por meio das APIs de áudio principal. Além disso, alguns aplicativos de áudio se comunicam diretamente com as APIs de áudio principais.

As APIs de áudio principais dão suporte à noção amigável de um dispositivo de ponto de extremidade de áudio. Um dispositivo de ponto de extremidade de áudio é uma abstração de software que representa um dispositivo físico que o usuário manipula diretamente. Exemplos de dispositivos de ponto de extremidade de áudio são palestrantes, fones de ouvido e microfones. Para obter mais informações, consulte [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).

O diagrama a seguir mostra as principais APIs de áudio e sua relação com os outros componentes de áudio no modo de usuário no Windows Vista.

![diagrama de componentes de renderização de áudio no modo de usuário](images/fig1.jpg)

Para simplificar, o diagrama anterior mostra apenas um caminho de dados de renderização de áudio para o dispositivo de ponto de extremidade — o diagrama não mostra um caminho de dados de captura de áudio. As principais APIs de áudio incluem a API do [MMDevice](mmdevice-api.md), a [WASAPI](wasapi.md), a [API do DeviceTopology](devicetopology-api.md)e a API do [EndpointVolume](endpointvolume-api.md), que são implementadas no Audioses.dll e Mmdevapi.dll módulos do sistema do modo de usuário.

Conforme mostrado no diagrama anterior, as APIs de áudio de núcleo fornecem uma base para as seguintes APIs de nível superior:

-   Media Foundation
-   Funções de **waveXxx** e **mixerXxx** multimídia do Windows
-   DirectSound
-   DirectMusic

O DirectSound, as funções de áudio de multimídia do Windows e Media Foundation (por meio de seu componente de processamento de áudio de streaming ou SAR) se comunicam diretamente com as APIs de áudio principais. O DirectMusic se comunica com as APIs de áudio principais indiretamente por meio do DirectSound.

Um cliente do WASAPI passa dados para um dispositivo de ponto de extremidade por meio de um *buffer de ponto de extremidade*. Os componentes de software e hardware do sistema gerenciam a movimentação de dados do buffer de ponto de extremidade para o dispositivo de ponto de extremidade de forma muito transparente para o cliente. Além disso, para um dispositivo de ponto de extremidade que se conecta a um adaptador de áudio com detecção de presença de tomada, o cliente pode criar um buffer de ponto de extremidade somente para um dispositivo de ponto de extremidade fisicamente presente. Para obter mais informações sobre a detecção de presença de Jack, consulte [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).

O diagrama anterior mostra dois tipos de buffer de ponto de extremidade. Se um cliente do WASAPI abrir um fluxo no *modo compartilhado*, o cliente gravará dados de áudio no buffer de ponto de extremidade e o mecanismo de áudio do Windows lerá os dados do buffer. Nesse modo, o cliente compartilha o hardware de áudio com outros aplicativos em execução em outros processos. O mecanismo de áudio combina os fluxos desses aplicativos e reproduz a combinação resultante através do hardware. O mecanismo de áudio é um componente do sistema de modo de usuário (Audiodg.dll) que executa todas as suas operações de processamento de fluxo no software. Por outro lado, se um cliente abrir um fluxo em *modo exclusivo*, o cliente terá acesso exclusivo ao hardware de áudio. Normalmente, apenas um pequeno número de aplicativos de "áudio pro" ou RTC requer o modo exclusivo. Embora o diagrama mostre o modo compartilhado e os fluxos de modo exclusivo, apenas um desses dois fluxos (e seu buffer de ponto de extremidade correspondente) existe, dependendo se o cliente abre o fluxo no modo compartilhado ou em modo exclusivo.

Em modo exclusivo, o cliente pode optar por abrir o fluxo em qualquer formato de áudio ao qual o dispositivo de ponto de extremidade dá suporte. No modo compartilhado, o cliente deve abrir o fluxo no formato de combinação que está atualmente em uso pelo mecanismo de áudio (ou um formato semelhante ao formato da combinação). Os fluxos de entrada do mecanismo de áudio e a combinação de saída do mecanismo estão todos neste formato.

No Windows 7, um novo recurso chamado *modo Low-latence* foi adicionado para fluxos no modo de compartilhamento. Nesse modo, o mecanismo de áudio é executado no modo de pull, no qual há uma redução significativa na latência. Isso é muito útil para aplicativos de comunicação que exigem baixa latência de fluxo de áudio para streaming mais rápido.

Os aplicativos que gerenciam fluxos de áudio de baixa latência podem usar o serviço do Agendador de classes de multimídia (MMCSS) no Windows Vista para aumentar a prioridade dos threads de aplicativo que acessam os buffers de ponto de extremidade. O MMCSS permite que os aplicativos de áudio sejam executados em alta prioridade sem negar recursos de CPU a aplicativos de prioridade mais baixa. O MMCSS atribui uma prioridade a um thread com base em seu nome de tarefa. Por exemplo, o Windows Vista dá suporte aos nomes de tarefas "áudio" e "áudio pro" para threads que gerenciam fluxos de áudio. Por padrão, a prioridade de um thread de "áudio pro" é maior do que a de um thread de "áudio". Para obter mais informações sobre o MMCSS, consulte a documentação do SDK do Windows.

As APIs de áudio principais dão suporte aos formatos de fluxo PCM e não PCM. No entanto, o mecanismo de áudio pode misturar somente fluxos PCM. Assim, somente os fluxos de modo exclusivo podem ter formatos não PCM. Para obter mais informações, consulte [formatos de dispositivo](device-formats.md).

O mecanismo de áudio é executado em seu próprio processo protegido, que é separado do processo em que o aplicativo é executado. Para dar suporte a um fluxo de modo compartilhado, o serviço de áudio do Windows (a caixa rotulada "serviço de áudio" no diagrama anterior) aloca um buffer de ponto de extremidade de processo cruzado que pode ser acessado pelo aplicativo e pelo mecanismo de áudio. Para o modo exclusivo, o buffer de ponto de extremidade reside na memória que é acessível ao aplicativo e ao hardware de áudio.

O serviço de áudio do Windows é o módulo que implementa a política de áudio do Windows. A política de áudio é um conjunto de regras internas que o sistema aplica às interações entre fluxos de áudio de vários aplicativos que compartilham e competem o uso do mesmo hardware de áudio. O serviço de áudio do Windows implementa a política de áudio definindo os parâmetros de controle para o mecanismo de áudio. As tarefas do serviço de áudio incluem:

-   Acompanhar os dispositivos de áudio que o usuário adiciona ou remove do sistema.
-   Monitorando as funções atribuídas aos dispositivos de áudio no sistema.
-   Gerenciar os fluxos de áudio de grupos de tarefas que produzem classes semelhantes de conteúdo de áudio (console, multimídia e comunicações).
-   Controlar o nível de volume do fluxo de saída combinado ("submix") para cada um dos vários tipos de conteúdo de áudio.
-   Informando o mecanismo de áudio sobre os elementos de processamento nos caminhos de dados para os fluxos de áudio.

Em algumas versões do Windows, o serviço de áudio do Windows está desabilitado por padrão e deve ser explicitamente ativado antes que o sistema possa reproduzir áudio.

No exemplo mostrado no diagrama anterior, o dispositivo de ponto de extremidade é um conjunto de alto-falantes que são conectados ao adaptador de áudio. O aplicativo cliente grava dados de áudio no buffer de ponto de extremidade, e o mecanismo de áudio manipula os detalhes de transporte dos dados do buffer para o dispositivo de ponto de extremidade.

A caixa rotulada "driver de áudio" no diagrama anterior pode ser uma combinação de componentes de driver fornecidos pelo sistema e pelo fornecedor. No caso de um adaptador de áudio em um barramento PCI ou PCI Express, o sistema fornece o driver de sistema de classe de porta (Portcls.sys), que implementa um conjunto de drivers de porta para as várias funções de áudio no adaptador, e o fornecedor de hardware fornece um driver de adaptador que implementa um conjunto de drivers de Miniport para lidar com operações específicas de dispositivo para os drivers de porta. No caso de um controlador de áudio de alta definição e um codec em um barramento PCI ou PCI Express, o sistema fornece o driver do adaptador (Hdaudio.sys) e nenhum driver fornecido pelo fornecedor é necessário. No caso de um adaptador de áudio em um barramento USB, o sistema fornece o driver de sistema de classe AVStream (Ks.sys) mais o driver de áudio USB (Usbaudio.sys); novamente, nenhum driver fornecido pelo fornecedor é necessário.

Para simplificar, o diagrama anterior mostra somente os fluxos de renderização. No entanto, as APIs de áudio de núcleo também dão suporte a fluxos de captura. No modo compartilhado, vários clientes podem compartilhar o fluxo capturado de um dispositivo de hardware de áudio. Em modo exclusivo, um cliente tem acesso exclusivo ao fluxo capturado do dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



