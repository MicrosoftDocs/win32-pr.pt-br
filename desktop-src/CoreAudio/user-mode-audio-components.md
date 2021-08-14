---
description: User-Mode de áudio
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8768cb6ece5825ae48803f30d8c1631a2e593f40815565b5dc879d23afd961aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166022"
---
# <a name="user-mode-audio-components"></a>User-Mode de áudio

No Windows Vista, as APIs de áudio principais servem como a base do subsistema de áudio no modo de usuário. As APIs de áudio principais são implementadas como uma camada fina de componentes do sistema de modo de usuário que separam clientes de modo de usuário de drivers de áudio de modo kernel e hardware de áudio. APIs de áudio de nível superior, como DirectSound e as funções Windows multimídia, acessam dispositivos de áudio por meio das APIs de áudio principais. Além disso, alguns aplicativos de áudio se comunicam diretamente com as APIs de áudio principais.

As APIs de áudio principais suportam a noção amigável de um dispositivo de ponto de extremidade de áudio. Um dispositivo de ponto de extremidade de áudio é uma abstração de software que representa um dispositivo físico que o usuário manipula diretamente. Exemplos de dispositivos de ponto de extremidade de áudio são alto-falantes, fones de ouvido e microfones. Para obter mais informações, consulte [Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).

O diagrama a seguir mostra as APIs de áudio principais e sua relação com os outros componentes de áudio do modo de usuário no Windows Vista.

![diagrama de componentes de renderização de áudio do modo de usuário](images/fig1.jpg)

Para simplificar, o diagrama anterior mostra apenas um caminho de dados de renderização de áudio para o dispositivo de ponto de extremidade — o diagrama não mostra um caminho de dados de captura de áudio. As APIs de áudio principais incluem a [API MMDevice,](mmdevice-api.md) [WASAPI,](wasapi.md) [a API DeviceTopology](devicetopology-api.md)e a API [EndpointVolume](endpointvolume-api.md), que são implementadas nos módulos do sistema Audioses.dll e Mmdevapi.dll modo de usuário.

Conforme mostrado no diagrama anterior, as APIs de áudio principais fornecem uma base para as seguintes APIs de nível superior:

-   Media Foundation
-   Windows funções **de multimídia waveXxx** e **mixerXxx**
-   Directsound
-   DirectMusic

DirectSound, o Windows funções de áudio multimídia e Media Foundation (por meio de seu renderador de áudio de streaming, ou SAR, componente) se comunicam diretamente com as APIs de áudio principais. O DirectMusic se comunica indiretamente com as APIs de áudio principais por meio do DirectSound.

Um cliente de WASAPI passa dados para um dispositivo de ponto de extremidade por meio de um *buffer de ponto de extremidade*. Os componentes de hardware e software do sistema gerenciam a movimentação de dados do buffer de ponto de extremidade para o dispositivo de ponto de extremidade de uma maneira amplamente transparente para o cliente. Além disso, para um dispositivo de ponto de extremidade que se conecta a um adaptador de áudio com detecção de presença de tomada, o cliente pode criar um buffer de ponto de extremidade somente para um dispositivo de ponto de extremidade que está fisicamente presente. Para obter mais informações sobre detecção de presença de jack, consulte [Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).

O diagrama anterior mostra dois tipos de buffer de ponto de extremidade. Se um cliente de WASAPI abrir um fluxo no modo compartilhado *,* o cliente grava dados de áudio no buffer do ponto de extremidade e o Windows de áudio lê os dados do buffer. Nesse modo, o cliente compartilha o hardware de áudio com outros aplicativos em execução em outros processos. O mecanismo de áudio combina os fluxos desses aplicativos e reproduz a combinação resultante por meio do hardware. O mecanismo de áudio é um componente do sistema de modo de usuário (Audiodg.dll) que executa todas as suas operações de processamento de fluxo no software. Por outro lado, se um cliente abrir um fluxo no *modo exclusivo*, o cliente terá acesso exclusivo ao hardware de áudio. Normalmente, apenas um pequeno número de aplicativos "pro audio" ou RTC exigem o modo exclusivo. Embora o diagrama mostre os fluxos de modo compartilhado e de modo exclusivo, apenas um desses dois fluxos (e seu buffer de ponto de extremidade correspondente) existe, dependendo se o cliente abre o fluxo no modo compartilhado ou no modo exclusivo.

No modo exclusivo, o cliente pode optar por abrir o fluxo em qualquer formato de áudio compatível com o dispositivo de ponto de extremidade. No modo compartilhado, o cliente deve abrir o fluxo no formato de combinação que está atualmente em uso pelo mecanismo de áudio (ou um formato semelhante ao formato de combinação). Os fluxos de entrada do mecanismo de áudio e a combinação de saída do mecanismo estão todos nesse formato.

No Windows 7, um novo  recurso chamado modo de baixa latência foi adicionado para fluxos no modo de compartilhamento. Nesse modo, o mecanismo de áudio é executado no modo de pull, no qual há uma redução significativa na latência. Isso é muito útil para aplicativos de comunicação que exigem baixa latência de fluxo de áudio para streaming mais rápido.

Aplicativos que gerenciam fluxos de áudio de baixa latência podem usar o MMCSS (Serviço de Agendador de Classes Multimídia) no Windows Vista para aumentar a prioridade de threads de aplicativo que acessam buffers de ponto de extremidade. O MMCSS permite que os aplicativos de áudio executem em alta prioridade sem negar recursos de CPU para aplicativos de prioridade mais baixa. O MMCSS atribui uma prioridade a um thread com base em seu nome de tarefa. Por exemplo, Windows Vista dá suporte aos nomes de tarefa "Áudio" e "Pro Áudio" para threads que gerenciam fluxos de áudio. Por padrão, a prioridade de um thread "Pro Áudio" é maior do que a de um thread "Áudio". Para obter mais informações sobre o MMCSS, consulte a documentação Windows SDK.

As APIs de áudio principais são suportadas em formatos de fluxo PCM e não PCM. No entanto, o mecanismo de áudio pode misturar apenas fluxos PCM. Portanto, somente fluxos de modo exclusivo podem ter formatos não PCM. Para obter mais informações, consulte [Formatos de dispositivo](device-formats.md).

O mecanismo de áudio é executado em seu próprio processo protegido, que é separado do processo em que o aplicativo é executado. Para dar suporte a um fluxo de modo compartilhado, o serviço de áudio Windows (a caixa rotulada como "Serviço de Áudio" no diagrama anterior) aloca um buffer de ponto de extremidade entre processos que pode ser acessado tanto para o aplicativo quanto para o mecanismo de áudio. Para o modo exclusivo, o buffer de ponto de extremidade reside na memória acessível ao aplicativo e ao hardware de áudio.

O Windows de áudio é o módulo que implementa Windows de áudio. A política de áudio é um conjunto de regras internas que o sistema se aplica às interações entre fluxos de áudio de vários aplicativos que compartilham e competem pelo uso do mesmo hardware de áudio. O Windows de áudio implementa a política de áudio definindo os parâmetros de controle para o mecanismo de áudio. As tarefas do serviço de áudio incluem:

-   Manter o controle dos dispositivos de áudio que o usuário adiciona ou remove do sistema.
-   Monitorando as funções atribuídas aos dispositivos de áudio no sistema.
-   Gerenciar os fluxos de áudio de grupos de tarefas que produzem classes semelhantes de conteúdo de áudio (console, multimídia e comunicações).
-   Controlar o nível de volume do fluxo de saída combinado ("submix") para cada um dos vários tipos de conteúdo de áudio.
-   Informando o mecanismo de áudio sobre os elementos de processamento nos caminhos de dados para os fluxos de áudio.

Em algumas versões do Windows, o Windows de áudio está desabilitado por padrão e deve ser explicitamente ligado antes que o sistema possa reproduzir áudio.

No exemplo mostrado no diagrama anterior, o dispositivo de ponto de extremidade é um conjunto de alto-falantes conectados ao adaptador de áudio. O aplicativo cliente grava dados de áudio no buffer do ponto de extremidade e o mecanismo de áudio lida com os detalhes do transporte dos dados do buffer para o dispositivo de ponto de extremidade.

A caixa rotulada "Driver de Áudio" no diagrama anterior pode ser uma combinação de componentes de driver fornecidos pelo sistema e fornecidos pelo fornecedor. No caso de um adaptador de áudio em um barramento PCI ou PCI Express, o sistema fornece o driver do sistema de classe de porta (Portcls.sys), que implementa um conjunto de drivers de porta para as várias funções de áudio no adaptador, e o fornecedor de hardware fornece um driver de adaptador que implementa um conjunto de drivers de miniporte para lidar com operações específicas do dispositivo para os drivers de porta. No caso de um controlador de áudio de alta definição e codec em um barramento PCI ou PCI Express, o sistema fornece o driver do adaptador (Hdaudio.sys) e nenhum driver fornecido pelo fornecedor é necessário. No caso de um adaptador de áudio em um barramento USB, o sistema fornece o driver de sistema de classe AVStream (Ks.sys) mais o driver de áudio USB (Usbaudio.sys); novamente, nenhum driver fornecido pelo fornecedor é necessário.

Para simplificar, o diagrama anterior mostra apenas fluxos de renderização. No entanto, as APIs de áudio principais também são suportadas por fluxos de captura. No modo compartilhado, vários clientes podem compartilhar o fluxo capturado de um dispositivo de hardware de áudio. No modo exclusivo, um cliente tem acesso exclusivo ao fluxo capturado do dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



