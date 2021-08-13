---
description: Depois que uma chamada estiver no estado conectado, as informações poderão ser transmitidas por ela.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Gerando dígitos e tons de inband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f144d4bc6b6273f71da37f6b9864146465c5ca29b91018a2e2ff097f6f19b44f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424876"
---
# <a name="generating-inband-digits-and-tones"></a>Gerando dígitos e tons de inband

Depois que uma chamada estiver no *estado* conectado, as informações poderão ser transmitidas por ela. Duas funções são fornecidas que permitem a sinalização de banda inband de ponta a ponta entre o aplicativo e o equipamento de estação remota, como um computador de resposta. Uma função é [**lineGenerateDigits,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)que gera dígitos de banda em uma chamada, sinalizando-os pelo canal de voz. Os dígitos podem ser sinalizados como sequências de rotação/pulso ou como tons DTMF. A outra função é [**lineGenerateTone,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)que permite que o aplicativo gere uma de uma variedade de inband de tons de multifrequência (por meio do fluxo de mídia). Isso gera tons de telefonia, como ringback, aviso de aviso e ocupado, bem como tons multifrequency e multicadenced arbitrários.

Apenas um dígito ou geração de tom pode estar em andamento em uma chamada a qualquer momento. Quando a geração de dígito ou tom é concluída, uma [**mensagem LINE \_ GENERATE**](line-generate.md) é enviada ao aplicativo que solicitou a geração. No caso em que vários dígitos são gerados, apenas uma única mensagem é enviada de volta depois que todos os dígitos são gerados. Chamar [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ou [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) enquanto a geração de dígito ou tom estiver em andamento anulará a geração em andamento e enviará a mensagem LINE GENERATE para o aplicativo cuja geração foi anulada com uma indicação de \_ cancelamento.

 

 



