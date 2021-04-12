---
title: O método setinfo
description: O método IADs setinfo salva os valores atuais das propriedades para esse Active Directory objeto do cache de propriedades para o repositório de diretório subjacente. Isso é análogo à liberação de um buffer para o disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- ADSI do setinfo, usando
- Propriedades ADSI, salve os valores atuais para propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291776"
---
# <a name="the-setinfo-method"></a>O método setinfo

O método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) salva os valores atuais das propriedades para esse Active Directory objeto do cache de propriedades para o repositório de diretório subjacente. Isso é análogo à liberação de um buffer para o disco.

[**Setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) atualiza objetos que já existem no diretório ou cria uma nova entrada de diretório para objetos recém-criados.

No momento da chamada [**setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , se algum valor de cache de propriedade tiver sido gravado com um código de controle [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) , como a propriedade ADS \_ \_ Update ou \_ ADS \_ Clear, as solicitações apropriadas serão passadas para o serviço de diretório subjacente.

 

 




