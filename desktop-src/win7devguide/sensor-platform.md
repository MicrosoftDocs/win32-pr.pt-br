---
title: Plataforma de sensor
description: O Windows 7 mudou como os desenvolvedores usam sensores.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007785"
---
# <a name="sensor-platform"></a>Plataforma de sensor

O Windows 7 mudou como os desenvolvedores usam sensores. Ele inclui suporte nativo para sensores, expandido por uma nova plataforma de desenvolvimento para trabalhar com sensores, incluindo sensores de localização, como dispositivos GPS (Global Positioning Systems).

Criado na plataforma do sensor, as APIs de *localização do Windows* são um novo recurso do Windows 7 que permite que os desenvolvedores de aplicativos acessem as informações de local físico do usuário. As APIs de *localização do Windows* podem abstrair hardware, dar suporte simultâneo a vários aplicativos e alternar diretamente entre diferentes tecnologias, aliviando o desenvolvedor do aplicativo da carga de gerenciar essas restrições. As APIs de *localização* podem ser usadas pelos programadores por meio da linguagem de programação C++ (por programadores familiarizados com Component Object Model (com)) ou usando objetos com em linguagens de script, como o Microsoft JScript. O suporte a scripts fornece fácil acesso a dados de localização para projetos como gadgets.

O Windows 7 fornece uma plataforma sólida e fácil de usar para usar dispositivos de sensor, como um sensor de luz ambiente ou um medidor de temperatura, para criar conscientização ambiental em aplicativos do Windows. Os computadores podem usar sensores que são incorporados ao computador, conectados por meio de conexões com ou sem fio, ou conectados por meio de uma rede ou da *Internet*.

As APIs do *sensor* e do *local* fornecem uma maneira padrão de descobrir sensores e acessar programaticamente os dados que os sensores fornecem.

O painel de controle do *sensor* permite que os usuários habilitem ou desabilitem sensores, controlem o acesso a sensores que podem expor dados confidenciais, exibir propriedades do sensor e alterar as descrições dos sensores.

A [extensão de classe de sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) é uma parte principal do modelo de desenvolvimento de driver para a plataforma do sensor. Ele fornece os seguintes mecanismos, que são usados ao escrever um driver de sensor de [estrutura de driver de modo de usuário (UMDF)](https://developer.microsoft.com/windows/hardware) :

-   Integração com a plataforma do sensor
-   Imposição de segurança

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de sensor](../sensorsapi/portal.md)
</dt> <dt>