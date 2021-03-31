---
title: Congelamento de eventos
description: Congelamento de eventos
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822582"
---
# <a name="event-freezing"></a>Congelamento de eventos

Um contêiner pode notificar um controle de que ele não está pronto para responder a eventos chamando [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **true**. Ele pode descongelar os eventos chamando **FreezeEvents** com **false**. Quando um contêiner congela eventos, está congelando o processamento de eventos, não o recebimento de eventos; ou seja, um contêiner ainda pode receber eventos enquanto os eventos são congelados. Se um contêiner receber uma notificação de eventos enquanto seus eventos estiverem congelados, o contêiner deverá ignorar o evento. Nenhuma outra ação é apropriada.

Um controle deve anotar a chamada de um contêiner para [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **true** se for importante para o controle que um evento não está perdido. Enquanto o processamento de eventos de um contêiner é congelado, um controle deve implementar uma das seguintes técnicas:

-   Dispare os eventos no conhecimento completo de que o contêiner não executará nenhuma ação.
-   Descartar todos os eventos que o controle teria disparado.
-   Enfileirar todos os eventos pendentes e disfire-los depois que o contêiner tiver chamado [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **false**.
-   Colocar em fila somente eventos relevantes ou importantes e disfire-los depois que o contêiner tiver chamado [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **false**.

Cada técnica é aceitável e apropriada em circunstâncias diferentes. O desenvolvedor de controle é responsável por determinar e implementar a técnica apropriada para a funcionalidade do controle.

 

 




