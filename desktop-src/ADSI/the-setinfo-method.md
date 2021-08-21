---
title: O método SetInfo
description: O método SETInfo de IADs salva os valores atuais para as propriedades desse objeto do Active Directory do cache de propriedades para o armazenamento de diretórios subjacente. Isso é análogo à liberação de um buffer para o disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI, usando
- propriedades ADSI , salve os valores atuais para propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e732cefa2d09b92f4fefec2b56f5f2ac8a99f77b2c7720822173cfaa647d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023134"
---
# <a name="the-setinfo-method"></a>O método SetInfo

O [**método IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) salva os valores atuais para as propriedades desse objeto do Active Directory do cache de propriedades para o armazenamento de diretórios subjacente. Isso é análogo à liberação de um buffer para o disco.

[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) atualiza objetos que já existem no diretório ou cria uma nova entrada de diretório para objetos recém-criados.

No momento da chamada [**SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) se algum valor de cache de propriedade tiver sido gravado com um código de controle [**PutEx,**](/windows/desktop/api/Iads/nf-iads-iads-putex) como ADS PROPERTY UPDATE ou ADS PROPERTY CLEAR, as solicitações apropriadas serão passadas para o serviço de diretório \_ \_ \_ \_ subjacente.

 

 




