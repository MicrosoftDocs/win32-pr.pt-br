---
description: Além de habilitar o monitoramento de dígitos e ser notificado de dígitos um de cada vez, um aplicativo também pode solicitar que vários dígitos sejam coletados em um buffer.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Coleta de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789873"
---
# <a name="digit-gathering"></a>Coleta de dígitos

Além de habilitar o monitoramento de dígitos e ser notificado de dígitos um de cada vez, um aplicativo também pode solicitar que vários dígitos sejam coletados em um buffer. Somente quando o buffer estiver cheio ou quando alguma outra condição de encerramento for atendida, o aplicativo será notificado. A coleta de dígitos é útil para funções como coleção de números de cartão de crédito. Ele é executado quando um aplicativo chama [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), especificando um buffer para preencher com dígitos. A coleta de dígitos é encerrada quando uma das seguintes condições é verdadeira:

-   O número de dígitos solicitado foi coletado.
-   Um dos vários dígitos de encerramento é detectado. Os dígitos de terminação são especificados para [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), e o dígito de término também é colocado no buffer.
-   Um dos dois tempos limite expira. Os tempos limites são um tempo limite de primeiro dígito, especificando a duração máxima antes que o primeiro dígito deve ser coletado e um tempo limite entre dígitos, especificando a duração máxima entre dígitos sucessivos.
-   A coleta de dígitos é cancelada explicitamente por [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) novamente com um outro conjunto de parâmetros para iniciar uma nova solicitação de coleta ou usando um parâmetro de buffer de dígito **nulo** para cancelar.

Quando a coleta de dígitos é encerrada por qualquer motivo, uma mensagem de [**\_ GATHERDIGITS de linha**](line-gatherdigits.md) é enviada ao aplicativo que solicitou a coleta de dígitos. Apenas uma solicitação de coleta de dígito único pode estar pendente em uma chamada a qualquer momento em todos os aplicativos que são proprietários da chamada.

A coleta de dígitos e o monitoramento de dígitos podem ser habilitados na mesma chamada ao mesmo tempo. Nesse caso, o aplicativo receberá uma mensagem [**de \_ MONITORDIGITS de linha**](line-monitordigits.md) para cada dígito detectado e uma mensagem de GATHERDIGITS de linha separada \_ quando o buffer for enviado de volta.

 

 



