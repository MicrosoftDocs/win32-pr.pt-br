---
title: Consultas de linha e controle de áudio
description: Consultas de linha e controle de áudio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- áudio de multimídia, controles de mixer
- áudio, controles de mixer
- mixers de áudio, linhas de áudio
- linhas de áudio
- mixers de áudio, controles
- mixers, controles
- mixers, linhas de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640546"
---
# <a name="audio-line-and-control-queries"></a>Consultas de linha e controle de áudio

Os serviços de mixer fornecem funções para determinar informações sobre linhas de áudio, controles de linha de áudio e detalhes de controle. Os serviços também fornecem funções para definir detalhes de controle.

Você pode usar a função [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) para recuperar informações sobre uma linha de áudio especificada. Essa função preenche a estrutura de [**mixer**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) para uma linha de áudio de origem especificada, uma linha de áudio de destino ou um identificador de linha. A estrutura inclui o número de linha de destino, o número de canais na linha de áudio, bem como um nome curto e longo para a linha de áudio.

A função [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera informações gerais sobre um ou mais controles associados a uma linha de áudio. Essa função preenche a estrutura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) com informações sobre o controle ou controles especificados. Você pode usar **mixerGetLineControls** para recuperar as propriedades de controle de um dos seguintes:

-   Todos os controles para uma linha de origem especificada
-   Um controle especificado para uma linha de origem especificada
-   O primeiro controle de uma classe específica para uma linha de origem especificada

A função [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera as propriedades de um único controle associado a uma linha de áudio. Essa função preenche a estrutura [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) com os valores atuais de um controle.

A função [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa o conteúdo da estrutura **MIXERCONTROLDETAILS** para definir as propriedades do controle especificado. Você deve garantir que todos os membros desta estrutura sejam preenchidos antes de chamar **mixerSetControlDetails**.

 

 