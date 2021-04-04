---
description: Um provedor de serviços pode indicar números de telefone gerados externamente definindo membros da estrutura LINECALLINFO ao processar a \_ função lineGetCallInfo do TSPI.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Números de telefone gerados externamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647178"
---
# <a name="externally-generated-phone-numbers"></a>Números de telefone gerados externamente

Um provedor de serviços pode indicar números de telefone gerados externamente (ou seja, números para chamadas de saída geradas externamente para o computador) definindo os membros **DisplayableAddress**, **CalledParty** ou [comment](./comment-ovr.md) na estrutura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) ao processar a função [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) . Se a TAPI não tiver salvo seus próprios dados para esses membros, ele deixará os dados definidos pelo provedor de serviços inalterados. Se a TAPI tiver dados armazenados em cache para esses membros, a TAPI adicionará seu texto ao final da parte variável da estrutura **LINECALLINFO** e substituirá o tamanho e o deslocamento que o provedor de serviços colocou na parte fixa.

Um provedor de serviços também pode copiar um número de saída para o membro **chamadoid** . Portanto, os aplicativos de log devem verificar o membro **chamadoid** nas chamadas de saída se os membros **DisplayableAddress** e **CalledParty** estiverem vazios.

 

 
