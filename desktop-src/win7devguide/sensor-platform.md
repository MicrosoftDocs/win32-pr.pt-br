---
title: Plataforma sensor
description: Windows 7 mudou a maneira como os desenvolvedores usam sensores.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7072a19ee0a746b0764850230a06de1ca72be8ca4633f1350165297f1ef4036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203886"
---
# <a name="sensor-platform"></a>Plataforma sensor

Windows 7 mudou a maneira como os desenvolvedores usam sensores. Ele inclui suporte nativo para sensores, expandido por uma nova plataforma de desenvolvimento para trabalhar com sensores, incluindo sensores de localização, como dispositivos GPS (Sistemas de Posicionamento Global).

Criadas na Plataforma de Sensor, as APIs de Windows *local* são um novo recurso Windows 7 que permite que os desenvolvedores de aplicativos acessem as informações de localização física do usuário. As APIs Windows *Local* do Windows podem abstrair o hardware, dar suporte simultaneamente a vários aplicativos e alternar perfeitamente entre diferentes tecnologias, aliviando o desenvolvedor de aplicativos da carga de gerenciamento dessas restrições. As APIs de Localização podem ser usadas por programadores por meio da linguagem de programação C++ (por programadores familiarizados com Component Object Model (COM)) ou usando objetos COM em linguagens de script, como o Microsoft JScript. O suporte a scripts fornece acesso fácil aos dados de localização para projetos como buges.

Windows 7 fornece uma plataforma sólida e fácil de usar para usar dispositivos de sensor, como um sensor de luz ambiente ou um medidor de temperatura, para criar reconhecimento ambiental em Windows aplicativos. Os computadores podem usar sensores internos no computador, conectados por meio de conexões com ou sem fio ou conectados por meio de uma rede ou da *Internet.*

As *APIs* *sensor e local* fornecem uma maneira padrão de descobrir sensores e acessar programaticamente os dados que os sensores fornecem.

O *painel de* controle Sensor permite que os usuários habilitam ou desabilitem sensores, controlam o acesso a sensores que podem expor dados confidenciais, exibir propriedades do sensor e alterar as descrições dos sensores.

A [Extensão de Classe do Sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) é uma parte fundamental do modelo de desenvolvimento de driver para a Plataforma de Sensor. Ele fornece os seguintes mecanismos, que são usados ao escrever um driver de sensor [do UMDF (User-Mode Driver Framework)](https://developer.microsoft.com/windows/hardware) :

-   Integração com a Plataforma de Sensor
-   Imposição de segurança

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de sensor](../sensorsapi/portal.md)
</dt> <dt>