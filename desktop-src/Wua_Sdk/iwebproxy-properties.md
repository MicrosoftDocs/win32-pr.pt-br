---
description: A interface IWebProxy define as propriedades a seguir.
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: Propriedades de IWebProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0dd5c6600f7fb8593f5cd47f5d02a45a84689bccb206359b8db8ffe6b320b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049124"
---
# <a name="iwebproxy-properties"></a>Propriedades de IWebProxy

A interface [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) define as propriedades a seguir.



| Propriedade                                                   | Descrição                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Endereço**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | Obtém e define o endereço e o número da porta decimal do servidor proxy.                                                |
| [**Autodetect**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | Obtém e define um valor booliana que indica se [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) detecta automaticamente as configurações de proxy. |
| [**Bypasslist**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | Obtém e define uma coleção de endereços que não usam o servidor proxy.                                                 |
| [**BypassProxyOnLocal**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | Obtém e define um valor booliana que indica se os endereços locais ignoram o servidor proxy.                             |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | Obtém um valor booliana que indica se o [**objeto WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) é somente leitura.                        |
| [**Username**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | Obtém e define o nome de usuário a ser enviar ao servidor proxy para autenticação.                                             |



 

 

 



