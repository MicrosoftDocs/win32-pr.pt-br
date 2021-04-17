---
description: Controle dos pais disponibilidade de SKU
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Controle dos pais disponibilidade de SKU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761221"
---
# <a name="parental-controls-sku-availability"></a>Controle dos pais disponibilidade de SKU

Os pais controlam as interfaces do usuário, os recursos e as APIs descritas nesta seção estão atualmente planejados para estar disponíveis somente em SKUs com foco no consumidor, como:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

Os controles dos pais são instalados apenas nessas SKUs. As soluções que têm um requisito para implantar em SKUs de negócios precisarão:

-   Detectar e não fornecer a funcionalidade de controles dos pais em SKUs de negócios.
-   Detecte e forneça um meio alternativo de configuração, registro em log e restrições.

É recomendável que as soluções detectem a disponibilidade da infraestrutura de controles dos pais verificando o êxito de COM CoCreateInstance na API de conformidade.

Os aplicativos com reconhecimento de controles pelos pais, dependendo da infraestrutura do Windows Vista, também podem querer suprimir qualquer uma de suas próprias configurações de exposição da interface do usuário ou outras funcionalidades quando a interface do usuário de controles dos pais for suprimida em uma SKU com suporte. Uma função é fornecida para determinação de visibilidade que abrange casos como supressão ingressada no domínio.

 

 



