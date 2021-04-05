---
description: Sobre as APIs de áudio do Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Sobre as APIs de áudio do Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826677"
---
# <a name="about-the-windows-core-audio-apis"></a>Sobre as APIs de áudio do Windows Core

Esta documentação fornece informações sobre as principais APIs de áudio para a família Microsoft Windows de sistemas operacionais.

As principais APIs de áudio foram introduzidas no Windows Vista. Este é um novo conjunto de componentes de áudio do modo de usuário que fornece aplicativos cliente com recursos de áudio aprimorados. Esses recursos incluem o seguinte:

-   Streaming de áudio de baixa latência e resistente a falhas.
-   Confiabilidade aprimorada (muitas funções de áudio foram movidas do modo kernel para o modo de usuário).
-   Segurança aprimorada (o processamento de conteúdo de áudio protegido ocorre em um processo seguro e de baixo privilégio).
-   Atribuição de funções específicas de todo o sistema (console, multimídia e comunicações) a dispositivos de áudio individuais.
-   Abstração de software dos dispositivos de ponto de extremidade de áudio (por exemplo, alto-falantes, fones de ouvido e microfones) que o usuário manipula diretamente.

As principais APIs de áudio foram aprimoradas no Windows 7. Para obter mais informações sobre os aprimoramentos e novos recursos adicionados, consulte [novidades para APIs de áudio de núcleo no Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

Esta documentação descreve as principais APIs de áudio. Essas APIs servem como base para as seguintes APIs de nível superior:

-   DirectSound
-   DirectMusic
-   Funções de **waveXxx** e **mixerXxx** multimídia do Windows
-   Media Foundation

Essas APIs de nível superior usam as principais APIs de áudio para compartilhar o acesso a dispositivos de áudio. Media Foundation é novo no Windows Vista, enquanto o DirectSound, o DirectMusic e as funções **waveXxx** e **mixerXxx** têm suporte no Windows 98, no Windows Millennium Edition e no Windows 2000 e posterior.

A maioria dos aplicativos de áudio se comunica com as APIs de nível superior em vez de se comunicar diretamente com as APIs de áudio principais. Alguns exemplos de aplicativos que usam APIs de nível superior são:

-   Players de mídia
-   Players de DVD
-   Jogos
-   Aplicativos de negócios, como Microsoft Office PowerPoint, que reproduzem arquivos de som

Normalmente, esses aplicativos se comunicam com as APIs DirectSound ou Media Foundation.

A comunicação direta com as APIs de áudio principais pode não ser adequada para muitos aplicativos de áudio de uso geral. Por exemplo, as APIs de áudio principais exigem fluxos de áudio para usar os formatos de dados nativos de um dispositivo de áudio. No entanto, os desenvolvedores de software de terceiros que estão desenvolvendo os seguintes tipos de produtos podem exigir os recursos especiais das APIs de áudio principal:

-   Aplicativos de áudio profissional ("áudio pro")
-   Aplicativos de comunicação em tempo real (RTC)
-   APIs de áudio de terceiros

Um aplicativo de "áudio pro" ou RTC pode precisar de acesso direto aos recursos de baixo nível das APIs de áudio principal para obter a latência mínima ao obter acesso exclusivo ao hardware de áudio. Uma API de áudio de terceiros pode exigir acesso direto às APIs de áudio principais para implementar um conjunto de recursos que podem não ser totalmente suportados por qualquer API de áudio de alto nível fornecida com o Windows.

Um aplicativo que usa uma API de áudio herdada para reproduzir ou gravar áudio pode exigir recursos adicionais que não têm suporte da API de áudio herdada, mas que têm suporte das APIs de áudio de núcleo. Em muitos casos, o aplicativo pode acessar esses recursos diretamente por meio das APIs de áudio principais, que podem ser usadas em conjunto com a API de áudio herdada.

As principais APIs de áudio são:

-   [API do dispositivo de multimídia (MMDevice)](mmdevice-api.md). Os clientes usam essa API para enumerar os dispositivos de ponto de extremidade de áudio no sistema.
-   [API de sessão de áudio do Windows (WASAPI)](wasapi.md). Os clientes usam essa API para criar e gerenciar fluxos de áudio de e para dispositivos de ponto de extremidade de áudio.
-   [API DeviceTopology](devicetopology-api.md). Os clientes usam essa API para acessar diretamente os recursos do topológica (por exemplo, controles de volume e multiplexadores) que se encontram nos caminhos de dados dentro de dispositivos de hardware em adaptadores de áudio.
-   [API EndpointVolume](endpointvolume-api.md). Os clientes usam essa API para acessar diretamente os controles de volume em dispositivos de ponto de extremidade de áudio. Essa API é usada principalmente por aplicativos que gerenciam fluxos de áudio de modo exclusivo.

Essas APIs oferecem suporte à noção amigável de um dispositivo de ponto de extremidade, que é descrita em [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).

A Microsoft não planeja fazer as APIs de áudio principal descritas aqui disponíveis para uso com versões anteriores do Windows, incluindo Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 e Windows 98.

Esta visão geral contém os tópicos a seguir.



| **Tópico**                                                                                      | **Descrição**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [O que há de novo para as APIs de áudio de núcleo no Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Resume os novos recursos e as melhorias nas APIs de áudio principais                   |
| [Arquivos de cabeçalho e componentes do sistema](header-files-and-system-components.md)                   | Descreve os arquivos de cabeçalho e componentes do sistema para as APIs de áudio principal.                 |
| [Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)       | Lista os exemplos no SDK do Windows que usam as APIs de áudio principal.                        |




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de áudio de núcleo](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



