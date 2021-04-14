---
title: CPROVCF. CPP
description: No componente do provedor de exemplo, um exemplo de código do código de fábrica da classe de objeto do provedor ADs está em cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453489"
---
# <a name="cprovcfcpp"></a>CPROVCF. CPP

No componente do provedor de exemplo, um exemplo de código do código de fábrica da classe de objeto do provedor ADs está em cprovcf. cpp. O componente de provedor nunca cria diretamente uma instância desse objeto a qualquer momento além de quando o objeto é criado automaticamente durante as operações de associação em [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou a função interna no método de Visual Basic **GetObject**. O método com suporte é listado na tabela a seguir.



| Método                                  | Descrição                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF:: CreateInstance** | Cria uma instância da fábrica de classes para o objeto do provedor ADS. |



 

 

 




