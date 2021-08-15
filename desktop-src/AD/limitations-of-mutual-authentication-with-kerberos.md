---
title: Limitações da autenticação mútua com Kerberos
description: A conta do cliente e a conta do serviço devem estar em domínios de modo misto ou nativo do Windows 2000, pois os serviços Kerberos não estão disponíveis em domínios de nível baixo.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bdc2f8cfe87d3cece32987ee0958000b1186775257013ce27f5950c6ac8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187060"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitações da autenticação mútua com Kerberos

A conta do cliente e a conta do serviço devem estar em domínios de modo misto ou nativo do Windows 2000, pois os serviços Kerberos não estão disponíveis em domínios de nível baixo. Além disso, as contas de cliente e de serviço devem estar na mesma floresta porque o KDC do cliente usa o catálogo global para pesquisar o nome da entidade de serviço.

O serviço e o cliente devem estar em execução no Windows 2000; caso contrário, a autenticação mútua com Kerberos falhará porque as versões anteriores do Windows não são suportadas por Kerberos.

Os nomes de entidade de serviço devem incluir o nome DNS do servidor host no qual o serviço está em execução. Você deve usar o nome DNS.

 

 




