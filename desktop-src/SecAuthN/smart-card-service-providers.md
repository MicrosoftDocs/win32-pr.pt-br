---
description: Os provedores de serviço de cartão inteligente (SCSP) fornecem acesso a recursos de cartão inteligente.
ms.assetid: f214385f-3e65-4175-925c-3d1dc4060185
title: Provedores de serviço de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc60e9987912426fcca3f6605b9218e085e61ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752621"
---
# <a name="smart-card-service-providers"></a>Provedores de serviço de cartão inteligente

Os provedores de serviço de cartão inteligente (SCSP) fornecem acesso a recursos de [*cartão inteligente*](../secgloss/s-gly.md) . Eles podem fornecer acesso a um único recurso, como os provedores de serviço base fornecidos pelo SDK do cartão inteligente, ou podem fornecer acesso a vários recursos para realizar uma tarefa mais complexa.

Os provedores de serviço fornecem acesso por meio de interfaces COM. O SDK do cartão inteligente fornece as interfaces COM usadas por seus próprios provedores de serviço base, bem como várias interfaces de aplicativo que podem ser usadas ao desenvolver provedores de serviços personalizados.



| Tópico                                                                                   | Descrição                                            |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Provedores de serviço base](base-service-providers.md)<br/>                         | Provedores de serviço base.<br/>                     |
| [Criando um comando APDU ISO7816-4](building-an-iso7816-4-apdu-command.md)<br/> | Adicionando funcionalidade a um provedor de serviços.<br/> |
| [Provedor de serviços de wrapper de fornecedor](vendor-wrapper-service-provider.md)<br/>       | Um exemplo de wrapper de fornecedor.<br/>                   |



 

Para obter uma visão geral de todas as interfaces COM fornecidas pelo SDK do cartão inteligente (provedor de serviços base e interfaces de aplicativo), consulte [interfaces de cartão inteligente](smart-card-interfaces.md).

 

 
