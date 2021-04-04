---
description: Os monitores recebem quadros de rede capturados no modo em tempo real. Os quadros são capturados por um NPP (provedor de pacotes de rede) usando a interface COM de provedores IRTC e passados para o monitor em um dos monitores dois threads de execução.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Capturas de Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837396"
---
# <a name="real-time-captures"></a>Capturas de Real-Time

Os monitores recebem quadros de rede capturados no modo em tempo real. Os quadros são capturados por um NPP ( [*provedor de pacotes de rede*](n.md) ) usando a interface com do [IRTC](irtc.md) do provedor e passados para o monitor em um dos dois threads de execução do monitor.

Os monitores podem limitar o número de quadros que precisam ser processados, passando um [*filtro de captura*](c.md) para o NPP que está fornecendo os quadros. Normalmente, um monitor específico é projetado para inspecionar tipos específicos de tráfego, como HTTP, RIPX ou SMB. Ao contrário de especialistas, que usam analisadores sofisticados para selecionar as informações a serem analisadas, um monitor deve examinar cada quadro para as condições que ele foi projetado para detectar. O motivo por trás dessa abordagem quadro a quadro é o desempenho. Um monitor deve processar seus quadros rapidamente o bastante para que ele não fique atrás do driver fornecendo os quadros para o NPP. Caso contrário, os dados serão perdidos.

 

 



