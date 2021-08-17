---
description: Disponibilidade de SKU dos Controles Dos Pais
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilidade de SKU dos Controles Dos Pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21184a383a28e3ae06198f203475c1c03334e5d678278bbb3b4988b52971e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461196"
---
# <a name="parental-controls-sku-availability"></a>Disponibilidade de SKU dos Controles Dos Pais

Atualmente, as interfaces do usuário, os recursos e as APIs dos Controles Dos Pais descritos nesta seção estão planejadas para estar disponíveis apenas em SKUs voltadas para o consumidor, como:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

Os Controles Dos Pais só são instalados nesses SKUs. As soluções que têm um requisito para implantar em SKUs de negócios precisarão:

-   Detectar e não fornecer a funcionalidade de controles dos pais em SKUs comerciais.
-   Detecte e forneça um meio alternativo de configuração, registro em log e restrições.

É recomendável que as soluções detectem a disponibilidade da Infraestrutura de Controles dos Pais verificando se há êxito da CoCreateInstance COM na API de Conformidade.

Os aplicativos com suporte para Controles Dos Pais, dependendo da infraestrutura do Windows Vista, também podem querer suprimir qualquer uma de suas próprias interfaces do usuário que expõem configurações ou outras funcionalidades quando a interface do usuário dos Controles Dos Pais é suprimida em um SKU com suporte. Uma função é fornecida para determinação de visibilidade que abrange casos como supressão ingressada no domínio.

 

 



