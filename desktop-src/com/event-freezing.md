---
title: Congelamento de eventos
description: Congelamento de eventos
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba439ebce12a48d78e1eb1d2daa31990c02f4a42082d3425e9b6ef2f842b3ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736796"
---
# <a name="event-freezing"></a>Congelamento de eventos

Um contêiner pode notificar um controle de que ele não está pronto para responder a eventos chamando [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **TRUE.** Ele pode descongelar os eventos chamando **FreezeEvents** com **FALSE.** Quando um contêiner congela eventos, ele congela o processamento de eventos, não o recebimento de eventos; ou seja, um contêiner ainda pode receber eventos enquanto os eventos são congelados. Se um contêiner receber uma notificação de evento enquanto seus eventos estão congelados, o contêiner deverá ignorar o evento. Nenhuma outra ação é apropriada.

Um controle deve anotar a chamada de um contêiner para [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **TRUE** se for importante para o controle de que um evento não é perdido. Embora o processamento de eventos de um contêiner seja congelado, um controle deve implementar uma das seguintes técnicas:

-   A fire os eventos com conhecimento completo de que o contêiner não tomará nenhuma ação.
-   Descarte todos os eventos que o controle teria disparado.
-   Enfileie todos os eventos pendentes e a fire-os depois que o contêiner tiver chamado [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **FALSE.**
-   Enfileie apenas eventos relevantes ou importantes e a fire-los depois que o contêiner tiver chamado [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **FALSE.**

Cada técnica é aceitável e apropriada em circunstâncias diferentes. O desenvolvedor de controle é responsável por determinar e implementar a técnica apropriada para a funcionalidade do controle.

 

 




