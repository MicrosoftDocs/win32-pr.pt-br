---
title: CPROVCF. CPP
description: No componente do provedor de exemplo, um exemplo de código do código de fábrica da classe de objeto do provedor ADs está em cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3b77ea7fe1b1d6fe946b9a8b509be33c11f2a075ee658ee305f0f7ba2d2c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023664"
---
# <a name="cprovcfcpp"></a>CPROVCF. CPP

No componente do provedor de exemplo, um exemplo de código do código de fábrica da classe de objeto do provedor ADs está em cprovcf. cpp. o componente de provedor nunca cria diretamente uma instância desse objeto a qualquer momento além de quando o objeto é criado automaticamente durante as operações de associação em [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou a função interna no método de Visual Basic **getobject**. O método com suporte é listado na tabela a seguir.



| Método                                  | Descrição                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF:: CreateInstance** | Cria uma instância da fábrica de classes para o objeto do provedor ADS. |



 

 

 




