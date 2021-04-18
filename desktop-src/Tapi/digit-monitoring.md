---
description: O monitoramento de dígitos monitora a chamada de dígitos.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Monitoramento de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761969"
---
# <a name="digit-monitoring"></a>Monitoramento de dígitos

O monitoramento de dígitos monitora a chamada de dígitos. A TAPI permite que os dígitos sejam sinalizados de acordo com dois métodos (modos de dígitos):

-   Dígitos de pulso são sinalizados como sequências de pulso ou rotativa. Para detecção, esses pulsos se manifestam como nada mais do que sequências de cliques audíveis. Dígitos de pulso válidos são ' 0 ' até ' 9 '.
-   Os dígitos DTMF são sinalizados como tons de DTMF (frequência dupla de dois tons). Os dígitos DTMF válidos são ' 0 ' por meio de ' 9 ', ' A '. ' B ', ' C', ' d', ' \* ' e ' \# '. O início e a borda inferior de dígitos DTMF podem ser monitorados.

Um aplicativo pode habilitar ou desabilitar o monitoramento de dígitos em uma chamada especificada com [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits). Quando o monitoramento de dígitos está habilitado, os dígitos detectados fazem com que o aplicativo seja notificado com a mensagem de [**linha \_ MONITORDIGITS**](line-monitordigits.md) . Essa mensagem fornece o identificador de chamada no qual o dígito foi detectado, bem como o valor de dígito e o modo de dígito. O escopo do monitoramento de dígitos é associado pelo tempo de vida da chamada. O monitoramento de dígitos em uma chamada termina assim que a chamada *se desconecta* ou fica *ociosa*.

 

 



