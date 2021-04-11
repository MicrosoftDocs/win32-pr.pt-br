---
description: Guia de Programação
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guia de programação de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164141"
---
# <a name="core-audio-programming-guide"></a>Guia de programação de áudio de núcleo

Esta seção de guia explica os conceitos e recursos das principais APIs de áudio do Windows Vista e descreve como usá-las na programação de aplicativos.

Esta seção contém os seguintes tópicos.



| Tópico                                                                                                                      | Descrição                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Componentes de áudio do modo de usuário](user-mode-audio-components.md)                                                               | Por meio das interfaces de nível baixo nas APIs de áudio principal, um cliente pode acessar os componentes do sistema que gerenciam e misturam fluxos de áudio.                                                                        |
| [Áudio do modo de usuário protegido (PUMA)](protected-user-mode-audio--puma-.md)                                                   | Descreve as atualizações para o PUMA (áudio do modo de usuário protegido), o mecanismo de áudio do modo de usuário no ambiente protegido (PE), que fornece um ambiente mais seguro para processamento e renderização de áudio.              |
| [Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)                                                                       | Um dispositivo de ponto de extremidade de áudio é uma abstração de software que permite interações amigáveis com dispositivos de áudio, como microfones e alto-falantes.                                                              |
| [Sessões de áudio](audio-sessions.md)                                                                                       | Uma sessão de áudio é uma abstração de software que permite que um cliente gerencie uma coleção de fluxos de áudio relacionados como uma única unidade.                                                                           |
| [Controles de volume](volume-controls.md)                                                                                     | O sistema integra suas configurações de volume baseadas em políticas com as configurações de volume do usuário de maneira lógica e consistente.                                                                                      |
| [Gerenciamento de fluxo](stream-management.md)                                                                                 | A API de sessão de áudio do Windows (WASAPI) fornece um cliente com um conjunto completo de métodos para criar e gerenciar fluxos de áudio.                                                                             |
| [Topologias de dispositivo](device-topologies.md)                                                                                 | A API DeviceTopology permite que um cliente descubra os controles de áudio que estão nos vários caminhos de dados no hardware de áudio.                                                                          |
| [Usando a interface IKsControl para acessar as propriedades de áudio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Um aplicativo de áudio especializado pode precisar usar a interface IKsControl para acessar as propriedades de um adaptador de áudio.                                                                                     |
| [Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)                                     | Os principais recursos das APIs de áudio principais do Windows Vista podem ser incorporados a aplicativos existentes que usam o DirectSound, o DirectShow e as funções **waveOutXxx** e **waveInXxx** de multimídia do Windows. |
| [Som espacial](spatial-sound.md)                                                                                         | Fornece orientação para usar o Windows Sonic, solução de nível de plataforma da Microsoft para suporte a sons espaciais no Xbox e no Windows, permitindo que as indicações de áudio surround e elevação (acima ou abaixo do ouvinte). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de áudio de núcleo](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



