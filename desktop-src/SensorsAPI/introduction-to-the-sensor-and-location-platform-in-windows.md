---
description: o sistema operacional Windows 7 fornece suporte interno para dispositivos de sensor.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: visão geral do sensor de Windows e da plataforma de localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4847d6d6137b91ce577cfce0dbc54cc8c6e19430e1318eaff145c24ce493af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889721"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>visão geral do sensor de Windows e da plataforma de localização

o sistema operacional Windows 7 fornece suporte interno para dispositivos de sensor. Isso inclui suporte para sensores de localização, como dispositivos GPS. como parte desse suporte, o sensor de Windows e a plataforma de localização fornecem uma maneira padrão para que os fabricantes de dispositivos exponham dispositivos de Sensor a desenvolvedores de software e consumidores. Ao mesmo tempo, a plataforma fornece aos desenvolvedores uma API padronizada e uma DDI (interface de driver de dispositivo) para trabalhar com sensores e dados de sensor.

## <a name="about-sensor-devices"></a>Sobre os dispositivos de sensor

Os sensores vêm em muitas configurações e, de uma determinada perspectiva, quase tudo que fornece dados sobre fenômenos físicos pode ser chamado de sensor. Embora normalmente consideremos os sensores como dispositivos de hardware, os sensores lógicos também podem fornecer informações por meio da emulação da funcionalidade do sensor no software ou firmware. Além disso, um único dispositivo de hardware pode conter vários sensores.

o Sensor de Windows e a plataforma de localização organizam sensores em *categorias*, que representam classes amplas de dispositivos de Sensor e *tipos*, que representam tipos específicos de sensores. Por exemplo, um sensor em um controlador de jogo de vídeo que detecta a posição e movimento da mão de um jogador (talvez para um jogo de boliche de vídeo) seria Categorizado como um sensor de orientação, mas seu tipo seria o acelerômetro de 3D. no código, Windows representa categorias e tipos usando guids (identificadores globais exclusivos), muitos dos quais são predefinidos. Os fabricantes de dispositivos podem criar novas categorias e tipos definindo e publicando novos GUIDs, quando necessário.

Os dispositivos de localização compõem uma categoria especialmente interessante. Agora, a maioria das pessoas está familiarizada com GPS (Global Positioning Systems). no Windows, um sensor GPS faz parte da categoria local. A categoria de localização pode incluir outros tipos de sensor. Alguns desses tipos de sensor são baseados em software, como um resolvedor de IP que fornece informações de local com base em um endereço de Internet, um triangulator de torre de telefone celular que determina o local com base no próximo Towers ou um provedor de local de rede Wi-Fi que lê informações de local do hub de rede sem fio conectado.

## <a name="about-the-platform"></a>Sobre a plataforma

o Sensor de Windows e a plataforma de localização consistem nos seguintes componentes de desenvolvedor e de usuário:

-   a DDI permite que Windows forneça uma maneira padrão para que os dispositivos de sensor se conectem ao computador e forneçam dados a outros subsistemas.
-   a API do Sensor de Windows fornece um conjunto de métodos, propriedades e eventos para trabalhar com sensores conectados e dados de Sensor.
-   a api de localização de Windows, que se baseia na api do Sensor de Windows, fornece um conjunto de objetos de programação, incluindo objetos de script, para trabalhar com informações de localização.
-   O painel de controle local e outros sensores permite que os administradores de computadores definam sensores, incluindo sensores de localização, para cada usuário.

As seções a seguir descrevem cada um desses componentes.

## <a name="architecture-diagram"></a>Diagrama da Arquitetura

O diagrama a seguir mostra a relação entre os componentes.

![diagrama de plataforma de sensor e local](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Interface de driver de dispositivo

os fabricantes de Sensor podem criar drivers de dispositivo para conectar sensores com o Windows 7. os drivers de dispositivo de Sensor são implementados usando o modelo de driver Windows dispositivos portáteis (WPD), que se baseiam no Windows estrutura de driver de modo de usuário (UMDF). Muitos drivers de dispositivo foram gravados usando essas estruturas. Como essas tecnologias são estabelecidas, os programadores experientes de driver de dispositivo encontrarão a gravação de um driver de sensor como uma tarefa familiar. A DDI do sensor usa interfaces e tipos de dados UMDF e WPD específicos e também define comandos e parâmetros WPD específicos para o sensor, onde é necessário. para obter mais informações sobre como criar drivers de dispositivo de sensor, consulte o Windows Driver Kit.

## <a name="sensor-api"></a>API do Sensor

A API do sensor permite que os desenvolvedores de C++ criem programas baseados em sensor usando um conjunto de interfaces COM. A API define interfaces para executar tarefas comuns de programação de sensor que incluem o gerenciamento de sensores por categoria, tipo ou ID, gerenciamento de eventos de sensor, trabalho com sensores individuais e coleções de sensores e trabalho com dados de sensor. o SDK do Windows inclui arquivos de cabeçalho, documentação, exemplos e ferramentas para ajudar a orientar os desenvolvedores de software sobre como usar sensores em Windows programas. Esta documentação descreve a API do sensor.

## <a name="location-api"></a>API de localização

Criado com base na API do sensor, a API de localização fornece uma maneira fácil de recuperar dados sobre a localização geográfica ao proteger a privacidade do usuário. A API de localização fornece sua funcionalidade por meio de um conjunto de interfaces COM que representam objetos. Esses objetos podem ser usados por programadores que entendem como usar o COM por meio da linguagem de programação C++ ou em linguagens de script, como JScript. O suporte a scripts fornece fácil acesso a dados de localização para projetos que são executados na zona do computador local, como gadgets. o SDK do Windows inclui arquivos de cabeçalho, documentação (incluindo documentação de referência de script), exemplos e ferramentas para ajudar a orientar os desenvolvedores de software e da Web a usar informações de localização em seus programas.

## <a name="location-and-other-sensors-control-panel"></a>Painel de controle local e outros sensores

o Windows 7 inclui um painel de controle que permite aos administradores de computadores habilitar ou desabilitar sensores em todo o sistema ou para cada usuário. Como alguns sensores podem expor dados confidenciais, essa interface do usuário oferece aos administradores o controle sobre se todos os programas têm acesso a cada sensor para cada usuário. Os usuários também podem exibir as propriedades do sensor e alterar a descrição do sensor que é exibida na interface do usuário.

O painel de controle também fornece uma página local padrão para permitir que os usuários forneçam seu local. Quando nenhum sensor estiver disponível, a plataforma usará o local fornecido pelo usuário. Os usuários podem fornecer campos de endereço cívicos, que incluem o endereço, a cidade, o estado ou a província e o país ou a região.

## <a name="related-topics"></a>Tópicos relacionados

[Sobre a API do sensor](about-the-sensor-api.md)

[Windows Site da central de desenvolvedores de hardware](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Centro de Desenvolvedores do Windows](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
