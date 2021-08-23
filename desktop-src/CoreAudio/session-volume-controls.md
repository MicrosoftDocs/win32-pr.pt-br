---
description: Controles de volume de sessão
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Controles de volume de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe45dce825dedd116c8f9c65684ac665eb6483f95dec3d247071f66408e8ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758886"
---
# <a name="session-volume-controls"></a>Controles de volume de sessão

Conforme explicado anteriormente, os clientes do WASAPI podem controlar individualmente o nível de volume de cada [sessão de áudio](audio-sessions.md). WASAPI aplica a configuração de volume para uma sessão de forma uniforme a todos os fluxos na sessão. Cada nível de volume é um valor no intervalo de 0,0 a 1,0, onde 0,0 indica silêncio e 1,0 indica o volume completo (sem atenuação).

Um cliente cria implicitamente uma sessão atribuindo o primeiro fluxo a essa sessão. O nível de volume padrão da nova sessão é 1,0. Conforme discutido anteriormente, o usuário pode ajustar o nível de volume da sessão por meio da interface do usuário de um programa de controle (por exemplo, SNDVOL) que é um cliente WASAPI. As configurações de controle são persistentes.

Além das configurações de volume controladas pelo cliente, o sistema aplica suas próprias configurações de volume a sessões. Essas configurações são baseadas na política de áudio e mudam dinamicamente em resposta a alterações nos fluxos que compõem a combinação de áudio global. Para obter mais informações sobre a política de áudio, consulte [componentes de áudio do modo de usuário](user-mode-audio-components.md).

O software do sistema que implementa o controle de volume para cada fluxo multiplica os exemplos de PCM no fluxo pelo nível de volume efetivo. O nível de volume efetivo é o resultado da multiplicação das configurações de volume do cliente e do sistema. Assim, a alteração resultante na amplitude do sinal é uma combinação linear dos níveis de volume do cliente e do sistema. Por exemplo, se o nível de volume do cliente for 0,8 e o nível de volume do sistema for 0,5, o nível de volume efetivo será (0,8)<sup>.</sup> (0,5) = 0,4.

Observe que a intensidade percebida não é linear em relação à amplitude de sinal. Em vez disso, a intensidade varia aproximadamente como o logaritmo do nível de volume v:

intensidade em decibéis = 20<sup>.</sup> log ₁ ₀ (v)

Portanto, a configuração v = 0,5 atenua a intensidade do sinal original (o sinal antes de o nível do volume ser aplicado) por 6 decibéis, a configuração de v = 0,25 atenua o sinal por 12 decibéis e assim por diante. Um nível de volume v = 1,0, correspondente a 0 decibéis, não altera o nível de sinal original.

Os aplicativos de áudio com interfaces de usuário para controlar o nível de volume normalmente exibem controles deslizantes que geram alterações na intensidade percebida que são linearmente proporcional às alterações na posição do controle deslizante. Para produzir uma relação linear entre a intensidade percebida e a posição do controle deslizante, o aplicativo deve definir uma relação não linear entre o nível de volume v e a posição do controle deslizante. Para obter mais informações, consulte [controles de volume de áudio cônico](audio-tapered-volume-controls.md).

Conforme explicado anteriormente, o programa de controle de volume do sistema, SNDVOL, exibe os controles deslizantes de volume para as sessões de áudio que estão jogando em cada dispositivo de renderização de áudio. Esses controles deslizantes aparecem na caixa de grupo rotulada **aplicativos** na janela SndVol. Normalmente, cada sessão contém todos os fluxos de reprodução de uma janela de aplicativo específica. Por meio dos controles deslizantes na janela SNDVOL, os usuários controlam os níveis de volume de aplicativos de áudio individuais.

Como regra geral, um aplicativo deve atribuir todos os seus fluxos de reprodução à mesma sessão de áudio. O WASAPI não impede que um aplicativo distribua seus fluxos de reprodução entre várias sessões. No entanto, a proliferação resultante de controles deslizantes de volume em SNDVOL pode confundir os usuários.

Como opção, uma janela de aplicativo pode exibir um controle deslizante de volume. O controle deslizante do aplicativo deve refletir o estado do controle deslizante SNDVOL correspondente em todos os momentos. Portanto, se o usuário alterar o nível de volume movendo o controle deslizante na janela do aplicativo, o controle deslizante correspondente na janela SNDVOL deverá se mover de forma inarmazenada com o controle deslizante do aplicativo. Da mesma forma, se o usuário mover o controle deslizante SNDVOL, o controle deslizante do aplicativo deverá se mover de maneira inigual ao controle deslizante SNDVOL.

Para dar suporte a esse comportamento, o WASAPI implementa a interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Quando o usuário move o controle deslizante do aplicativo, o aplicativo chama o método [**ISimpleAudioVolume:: SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) para ajustar o nível de volume da sessão adequadamente. O SNDVOL monitora as alterações de volume feitas por esse método e reflete as alterações nos controles deslizantes de volume que ele exibe. Além disso, um aplicativo pode receber notificações de alterações de volume de sessão que o usuário faz por meio do SNDVOL. Para essa finalidade, o aplicativo implementa uma interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra a interface com WASAPI. Depois disso, cada vez que o usuário altera o nível de volume da sessão por meio de SNDVOL, o aplicativo recebe uma chamada de notificação pelo método [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) . Para obter um exemplo de código que implementa uma interface **IAudioSessionEvents** , consulte [eventos de sessão de áudio](audio-session-events.md). Para obter um exemplo de código que registra uma interface **IAudioSessionEvents** , consulte [eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md).

A interface **ISimpleAudioVolume** aplica o mesmo nível de volume uniformemente a todos os canais em uma sessão de áudio. Embora essa interface deva atender aos requisitos de controle de volume da maioria dos aplicativos, alguns aplicativos podem exigir recursos de controle de volume mais especializados. A interface [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) controla o volume de um fluxo individual em uma sessão relativa a outros fluxos na sessão. O **IAudioStreamVolume** também permite que um cliente controle individualmente os níveis de volume de todos os canais no fluxo. Por exemplo, um aplicativo pode usar essa capacidade para obter efeitos de áudio, como simular a movimentação espacial de uma fonte de áudio, movendo o movimento da esquerda para a direita. Outra interface especializada, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), controla os níveis de volume dos canais individuais em uma sessão. Por exemplo, um aplicativo pode usar **IChannelAudioVolume** para implementar controles de saldo para um sistema de som stereophonic.

Os controles deslizantes de volume na caixa **aplicativos** no SNDVOL refletem apenas as alterações de volume feitas por meio da interface **ISimpleAudioVolume** . Eles não refletem as alterações de volume feitas por meio das interfaces **IAudioStreamVolume** e **IChannelAudioVolume** . Embora alguns aplicativos possam permitir que os usuários controlem as configurações de volume direta ou indiretamente por meio de **IAudioStreamVolume** e **IChannelAudioVolume**, os desenvolvedores devem evitar a apresentação de controles deslizantes de aplicativos para essas configurações de volume que os usuários provavelmente confundirão com os controles deslizantes de volume no SNDVOL. Caso contrário, um usuário pode mover um controle deslizante de aplicativo esperando ver a alteração refletida em um controle deslizante SNDVOL e ficar confuso quando nenhuma alteração ocorrer. Os desenvolvedores podem evitar esse problema por meio do design cuidadoso da interface do usuário.

O nível de volume efetivo de qualquer canal na sessão submix, como ouvido nos alto-falantes, é o produto dos quatro fatores de nível de volume a seguir:

-   Os níveis de volume por canal dos fluxos na sessão, que os clientes podem controlar por meio dos métodos na interface **IAudioStreamVolume** .
-   O nível de volume por canal da sessão, que os clientes podem controlar por meio dos métodos na interface **IChannelAudioVolume** .
-   O nível de volume mestre da sessão, que os clientes podem controlar por meio dos métodos na interface **ISimpleAudioVolume** .
-   O nível de volume baseado em políticas da sessão, que o sistema modifica dinamicamente à medida que a combinação global é alterada.

Cada um dos quatro fatores de nível de volume na lista anterior é um valor no intervalo de 0,0 a 1,0, em que 0,0 indica silêncio e 1,0 indica volume completo (sem atenuação). O nível de volume efetivo também é um valor no intervalo de 0,0 a 1,0.

O mecanismo de áudio aplica o nível de volume efetivo para cada canal aos canais em um fluxo antes de misturar o fluxo com os outros fluxos na sessão de áudio. Se os valores de exemplo em um canal excederem 0 decibéis depois que o mecanismo de áudio os multiplicar pelo nível de volume efetivo, o mecanismo cortará as amostras antes de adicioná-las à sessão submix.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles de volume](volume-controls.md)
</dt> </dl>

 

 



