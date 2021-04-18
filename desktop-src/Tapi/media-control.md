---
description: A mídia de uma sessão de comunicações é o formulário no qual os dados são transmitidos. Os controles de mídia permitem que um aplicativo reconheça uma variedade de tipos de mídia e ajuste os aspectos do fluxo de mídia, como o volume de transmissão de voz.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Controle de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dad56e3feef8493a70cf93152b225be2777848
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764757"
---
# <a name="media-control"></a>Controle de mídia

A mídia de uma sessão de comunicações é o formulário no qual os dados são transmitidos. Os controles de mídia permitem que um aplicativo reconheça uma variedade de tipos de mídia e ajuste os aspectos do fluxo de mídia, como o volume de transmissão de voz.

A disponibilidade do controle de mídia e das informações varia muito com o tipo de aplicativo TAPI, suporte ao provedor de serviços e o ambiente de comunicações local. O material a seguir fornece uma descrição geral do controle de mídia. A TAPI fornece uma estrutura flexível para a implementação de controles, de modo que os recursos mais interessantes geralmente serão específicos para um determinado provedor de serviços.

Sob a telefonia clássica, um aplicativo tinha muito pouco controle sobre o fluxo de mídia depois que um caminho de comunicação foi configurado. Os aplicativos TAPI 2 têm acesso a algumas funções que permitem que eles reconheçam e reajam a dígitos ou tons durante uma chamada, e eles podem usar a API de onda para exercer controle adicional sobre a mídia durante uma sessão de comunicações, mas, caso contrário, eles não têm acesso ao fluxo de mídia. Consulte a visão geral de [acesso à mídia](./media-access.md) TAPI 2,2 ou a visão geral de acesso à [mídia](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) do TSPI para uma revisão dessas funções.

A TAPI 3 apresenta os [provedores de serviços de mídia](about-the-media-service-provider-msp-.md), que aumentam de forma acentuada as informações e o controle sobre a mídia ou uma sessão de comunicação. Um aplicativo TAPI 3 pode acessar diretamente o [fluxo](stream-objects.md) de mídia de uma sessão. Um fluxo separado é criado para cada tipo de mídia envolvido na sessão, como voz ou vídeo. Alguns MSPs podem implementar controles de Subfluxo, que podem dividir os fluxos ainda mais, como por participante no caso do IPConf MSP.



| Funções TAPI 2. x                                          | Descrição                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Inicia a coleta de dígitos em buffer na chamada especificada.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Inicia a geração dos dígitos especificados na chamada especificada como tons de inband usando o modo de sinalização especificado. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Gera o tom de inband especificado na chamada especificada.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Habilita e desabilita a detecção sem buffer de dígitos recebidos na chamada.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Habilita e desabilita a detecção de tipos de mídia na chamada especificada.                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Habilita e desabilita a detecção de tons de inband na chamada.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Habilita e desabilita as ações de controle no fluxo de mídia associado à linha, ao endereço ou à chamada especificada.             |



 



| Interfaces ou métodos TAPI 3. x                               | Descrição                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Dá suporte a aplicativos herdados que devem se comunicar diretamente com um dispositivo.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Permite que um aplicativo descubra se um terminal criado por um TSP herdado (pré-TAPI 3) pode ser controlado usando a API de onda.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Permite que um aplicativo recupere informações em um fluxo; para iniciar, pausar ou parar o fluxo; para selecionar ou cancelar a seleção de terminais em um fluxo; e para obter uma lista de terminais selecionados no fluxo. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Permite que um aplicativo enumere, crie ou remova fluxos de mídia.                                                                                                                                   |



 

 

 
