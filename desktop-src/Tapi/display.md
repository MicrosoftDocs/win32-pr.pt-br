---
description: A TAPI fornece acesso a uma exibição de telefones.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090450"
---
# <a name="display"></a>Monitor

A TAPI fornece acesso à exibição de um telefone. A exibição é modelada como uma área alfanumérica com linhas e colunas. Os recursos de dispositivo de um telefone indicam o tamanho da exibição de um telefone como o número de linhas e o número de colunas. Ambos os números serão zero se o dispositivo de telefone não tiver uma exibição. Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) para gravar informações na exibição de um dispositivo de telefone aberto e [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) para recuperar o conteúdo atual da exibição de um telefone.

Quando a exibição de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada para a função de aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

 

 



