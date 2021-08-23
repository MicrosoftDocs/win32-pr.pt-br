---
description: Sobre as APIs Windows Core Audio
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Sobre as APIs Windows Core Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d5336522a681fc5f2d6e8ee5db0c17eacccfa46ea4cc4559bf00e6ea629031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018544"
---
# <a name="about-the-windows-core-audio-apis"></a>Sobre as APIs Windows Core Audio

Esta documentação fornece informações sobre apIs de áudio principais para a família Windows microsoft de sistemas operacionais.

As APIs de áudio principais foram introduzidas no Windows Vista. Esse é um novo conjunto de componentes de áudio no modo de usuário que fornece aos aplicativos cliente recursos de áudio aprimorados. Esses recursos incluem o seguinte:

-   Streaming de áudio resiliente a falhas de baixa latência.
-   Confiabilidade aprimorada (muitas funções de áudio foram movidas do modo kernel para o modo de usuário).
-   Segurança aprimorada (o processamento de conteúdo de áudio protegido ocorre em um processo seguro e de privilégio inferior).
-   Atribuição de funções específicas em todo o sistema (console, multimídia e comunicações) a dispositivos de áudio individuais.
-   Abstração de software dos dispositivos de ponto de extremidade de áudio (por exemplo, alto-falantes, fones de ouvido e microfones) que o usuário manipula diretamente.

As APIs de Áudio Principal foram aprimoradas Windows 7. Para obter mais informações sobre as melhorias e os novos recursos adicionados, consulte Novidades para APIs de áudio principais [no Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

Esta documentação descreve as APIs de áudio principais. Essas APIs servem como base para as seguintes APIs de nível superior:

-   Directsound
-   DirectMusic
-   Windows funções **de multimídia waveXxx** e **mixerXxx**
-   Media Foundation

Essas APIs de nível superior usam as APIs de Áudio Core para compartilhar o acesso a dispositivos de áudio. Media Foundation é uma novidade no Windows Vista, enquanto as funções DirectSound, DirectMusic e **waveXxx** e **mixerXxx** têm suporte no Windows 98, no Windows Millennium Edition e no Windows 2000 e posterior.

A maioria dos aplicativos de áudio se comunica com as APIs de nível superior em vez de se comunicar diretamente com as APIs de Áudio Principal. Alguns exemplos de aplicativos que usam APIs de nível superior são:

-   Players de mídia
-   Players de DVD
-   Jogos
-   Aplicativos de negócios, como Microsoft Office PowerPoint, que reproduzem arquivos de som

Normalmente, esses aplicativos se comunicam com o DirectSound ou Media Foundation APIs.

A comunicação direta com as APIs de Áudio Principal pode não ser adequada para muitos aplicativos de áudio de uso geral. Por exemplo, as APIs de áudio principais exigem fluxos de áudio para usar os formatos de dados nativos de um dispositivo de áudio. No entanto, desenvolvedores de software de terceiros que estão desenvolvendo os seguintes tipos de produtos podem exigir as funcionalidades especiais das APIs de Áudio Principal:

-   Professional aplicativos de áudio ("pro audio")
-   Aplicativos RTC (comunicação em tempo real)
-   APIs de áudio de terceiros

Um aplicativo "pro audio" ou RTC pode precisar de acesso direto aos recursos de baixo nível das APIs de Áudio Core para obter latência mínima obtendo acesso exclusivo ao hardware de áudio. Uma API de áudio de terceiros pode exigir acesso direto às APIs de Áudio Principal para implementar um conjunto de recursos que podem não ter suporte total por qualquer API de áudio de alto nível única fornecida com Windows.

Um aplicativo que usa uma API de áudio herdada para reproduzir ou gravar áudio pode exigir funcionalidades adicionais que não têm suporte da API de áudio herdada, mas que têm suporte nas APIs de Áudio Core. Em muitos casos, o aplicativo pode acessar esses recursos diretamente por meio das APIs de Áudio Principal, que podem ser usadas em conjunto com a API de áudio herdada.

As APIs de áudio principais são:

-   [API de dispositivo multimídia (MMDevice).](mmdevice-api.md) Os clientes usam essa API para enumerar os dispositivos de ponto de extremidade de áudio no sistema.
-   [Windows API de Sessão de Áudio (WASAPI)](wasapi.md). Os clientes usam essa API para criar e gerenciar fluxos de áudio de e para dispositivos de ponto de extremidade de áudio.
-   [API DeviceTopology](devicetopology-api.md). Os clientes usam essa API para acessar diretamente os recursos topologias (por exemplo, controles de volume e multiplexadores) que estão ao longo dos caminhos de dados dentro de dispositivos de hardware em adaptadores de áudio.
-   [EndpointVolume API](endpointvolume-api.md). Os clientes usam essa API para acessar diretamente os controles de volume em dispositivos de ponto de extremidade de áudio. Essa API é usada principalmente por aplicativos que gerenciam fluxos de áudio de modo exclusivo.

Essas APIs são compatíveis com a noção amigável de um dispositivo de ponto de extremidade, que é descrita em Dispositivos [de Ponto de Extremidade de Áudio](audio-endpoint-devices.md).

A Microsoft não planeja disponibilizar as APIs de áudio principais descritas aqui para uso com versões anteriores do Windows, incluindo o Microsoft Windows Server 2003, o Windows XP, o Windows Millennium Edition, o Windows 2000 e o Windows 98.

Esta visão geral contém os tópicos a seguir.



| **Tópico**                                                                                      | **Descrição**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Novidades das APIs de áudio principal no Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Resume os novos recursos e os aprimoramentos para as APIs de Áudio Principal                   |
| [Arquivos de header e componentes do sistema](header-files-and-system-components.md)                   | Descreve os arquivos de header e os componentes do sistema para as APIs de Áudio Core.                 |
| [Exemplos de SDK que usam as APIs de áudio principais](sdk-samples-that-use-the-core-audio-apis.md)       | Lista os exemplos no SDK Windows que usam as APIs de Áudio Principal.                        |




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de áudio principais](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



