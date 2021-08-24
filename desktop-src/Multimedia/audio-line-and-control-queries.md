---
title: Linhas de áudio e consultas de controle
description: Linhas de áudio e consultas de controle
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- áudio multimídia, controles de mixer
- áudio, controles de mixer
- mixers de áudio, linhas de áudio
- linhas de áudio
- mixers de áudio, controles
- mixers,controls
- mixers, linhas de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c417b55273ba3f7f96cd857979c73003ed0f88c2161e1c2ac14d934fddcff1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692106"
---
# <a name="audio-line-and-control-queries"></a>Linhas de áudio e consultas de controle

Os serviços de mixer fornecem funções para determinar informações sobre linhas de áudio, controles de linha de áudio e detalhes de controle. Os serviços também fornecem funções para definir detalhes de controle.

Você pode usar a [**função mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) para recuperar informações sobre uma linha de áudio especificada. Essa função preenche a estrutura [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) para uma linha de áudio de origem especificada, linha de áudio de destino ou identificador de linha. A estrutura inclui o número da linha de destino, o número de canais na linha de áudio, bem como um nome curto e longo para a linha de áudio.

A [**função mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera informações gerais sobre um ou mais controles associados a uma linha de áudio. Essa função preenche a estrutura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) com informações sobre o controle ou os controles especificados. Você pode usar **mixerGetLineControls** para recuperar propriedades de controle para um dos seguintes:

-   Todos os controles para uma linha de origem especificada
-   Um controle especificado para uma linha de origem especificada
-   O primeiro controle de uma classe específica para uma linha de origem especificada

A [**função mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera propriedades de um único controle associado a uma linha de áudio. Essa função preenche a estrutura [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) com os valores atuais de um controle.

A [**função mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa o conteúdo da estrutura **MIXERCONTROLDETAILS** para definir as propriedades do controle especificado. Você deve garantir que todos os membros dessa estrutura sejam preenchidos antes de chamar **mixerSetControlDetails.**

 

 