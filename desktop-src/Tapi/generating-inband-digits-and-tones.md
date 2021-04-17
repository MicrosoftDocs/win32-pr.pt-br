---
description: Depois que uma chamada está no estado conectado, as informações podem ser transmitidas sobre ela.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Gerando dígitos de banda e tons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766231"
---
# <a name="generating-inband-digits-and-tones"></a>Gerando dígitos de banda e tons

Depois que uma chamada está no estado *conectado* , as informações podem ser transmitidas sobre ela. São fornecidas duas funções que permitem a sinalização de faixa de ponta a ponta entre o aplicativo e equipamentos de estação remota, como uma secretária eletrônica. Uma função é [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), que gera dígitos de inband em uma chamada, sinalizando-os pelo canal de voz. Os dígitos podem ser sinalizados como sequências rotativa/pulso ou como tons DTMF. A outra função é [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), que permite que o aplicativo gere um de vários tons de várias frequências (sobre o fluxo de mídia). Isso gera tons de telefonia, como, por exemplo, toque, alarme sonoro e ocupado, bem como tons arbitrários de multifrequências e multicadências.

Somente uma geração de dígito ou Tom pode estar em andamento em uma chamada a qualquer momento. Quando a geração de dígitos ou tons é concluída, uma mensagem de [**\_ geração de linha**](line-generate.md) é enviada para o aplicativo que solicitou a geração. No caso em que vários dígitos são gerados, apenas uma única mensagem é enviada de volta após a geração de todos os dígitos. Chamar [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ou [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) enquanto a geração de dígito ou Tom está em andamento anulará a geração atualmente em andamento e enviará a mensagem de geração de linha \_ para o aplicativo cuja geração foi anulada com uma indicação de cancelamento.

 

 



