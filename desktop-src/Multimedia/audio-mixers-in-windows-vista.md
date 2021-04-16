---
title: Mixers de áudio no Windows Vista
description: Mixers de áudio no Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- áudio multimídia, mixers de áudio do Windows Vista
- áudio, mixers de áudio do Windows Vista
- mixers de áudio, Windows Vista
- mixers, Windows Vista
- Mixers de áudio do Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104558762"
---
# <a name="audio-mixers-in-windows-vista"></a>Mixers de áudio no Windows Vista

A partir do Windows Vista, alguns controles de mixer são implementados em software em vez de hardware. Por exemplo, os controles de volume são implementados usando a API de sessão de áudio do Windows (WASAPI). Esses controles não afetam diretamente as configurações de hardware. Além disso, eles são associados a uma sessão de áudio específica do processo, portanto, as alterações afetam o aplicativo de chamada, mas não afetam outros aplicativos.

Cada dispositivo de ponto de extremidade de áudio tem um layout de mixer padrão, implementado no software.

-   Cada ponto de extremidade de renderização de áudio contém uma linha de destino que contém o seguinte:
    -   Controle de volume
    -   Controle sem áudio
    -   Linha de origem: onda-saída de áudio.
    -   Linha de origem: CD de áudio.
-   Cada ponto de extremidade de captura de áudio contém uma linha de destino que contém o seguinte:
    -   Controle de volume
    -   Controle sem áudio
    -   Linha de origem: formato de onda-entrada de áudio. O tipo de componente depende do dispositivo de entrada, por exemplo, um microfone.

Cada linha de origem contém um controle de volume e um controle sem áudio. O diagrama a seguir mostra os componentes de pontos de extremidade de renderização e captura de pontos de extremidade.

![layouts de mixer padrão](images/mixer1.gif)

Todos os controles de um ponto de extremidade manipulam o mesmo controle de software subjacente. Portanto, se você alterar as configurações em um controle, receberá uma notificação de alteração de controle nos outros controles. (Consulte [**\_ mudança de \_ controle \_ de MIXM mm**](mm-mixm-control-change.md).)

Esse layout padrão é fornecido para compatibilidade com os aplicativos existentes que usam as funções do mixer de áudio. Os novos aplicativos devem evitar o uso dessas funções.

 

 




