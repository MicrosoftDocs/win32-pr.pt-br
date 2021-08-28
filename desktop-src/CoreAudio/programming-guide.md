---
description: Saiba mais sobre os conceitos e recursos das PRINCIPAIS APIs de áudio do Windows Vista e como usá-los na programação de aplicativos.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guia de programação de áudio principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b8f65d0c5508cd821b49a42b4b89ea42859390913a30534319d5ef7c79224f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088386"
---
# <a name="core-audio-programming-guide"></a>Guia de programação de áudio principal

Esta seção de guia explica os conceitos e os recursos das PRINCIPAIS APIs de áudio do Windows Vista e descreve como usá-los na programação de aplicativos.

Esta seção contém os seguintes tópicos.



| Tópico                                                                                                                      | Descrição                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Componentes de áudio do modo de usuário](user-mode-audio-components.md)                                                               | Por meio das interfaces de baixo nível nas APIs de áudio principais, um cliente pode acessar os componentes do sistema que gerenciam e combinam fluxos de áudio.                                                                        |
| [Áudio de modo de usuário protegido (MOTION)](protected-user-mode-audio--puma-.md)                                                   | Descreve as atualizações do AUDIO (Modo de Usuário Protegido), o mecanismo de áudio de modo de usuário no PE (Ambiente Protegido), que fornece um ambiente mais seguro para processamento e renderização de áudio.              |
| [Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)                                                                       | Um dispositivo de ponto de extremidade de áudio é uma abstração de software que permite interações amigáveis com dispositivos de áudio, como microfones e alto-falantes.                                                              |
| [Sessões de áudio](audio-sessions.md)                                                                                       | Uma sessão de áudio é uma abstração de software que permite que um cliente gerencie uma coleção de fluxos de áudio relacionados como uma única unidade.                                                                           |
| [Controles de volume](volume-controls.md)                                                                                     | O sistema integra suas configurações de volume baseadas em políticas com as configurações de volume do usuário de maneira lógica e consistente.                                                                                      |
| [Gerenciamento de Fluxo](stream-management.md)                                                                                 | A API Windows de Sessão de Áudio (WASAPI) fornece a um cliente um conjunto completo de métodos para criar e gerenciar fluxos de áudio.                                                                             |
| [Topologias de dispositivo](device-topologies.md)                                                                                 | A API DeviceTopology permite que um cliente descubra os controles de áudio que estão ao longo dos vários caminhos de dados no hardware de áudio.                                                                          |
| [Usando a interface IKsControl para acessar propriedades de áudio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Um aplicativo de áudio especializado pode precisar usar a interface IKsControl para acessar as propriedades de um adaptador de áudio.                                                                                     |
| [Interoperabilidade com APIs de áudio herdado](interoperability-with-legacy-audio-apis.md)                                     | Os principais recursos das PRINCIPAIS APIs de áudio no Windows Vista podem ser incorporados em aplicativos existentes que usam o DirectSound, DirectShow e as funções **waveOutXxx** e **waveInXxx** multimídia do Windows. |
| [Som espacial](spatial-sound.md)                                                                                         | Fornece diretrizes para usar Windows Sonic, a solução de nível de plataforma da Microsoft para suporte a som espacial no Xbox e no Windows, permitindo habilitando as habilitações de áudio surround e elevação (acima ou abaixo do ouvinte). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de áudio principais](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



