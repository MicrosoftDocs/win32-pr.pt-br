---
title: Limitações de autenticação mútua com Kerberos
description: A conta do cliente e a conta do serviço devem estar em domínios do Windows 2000 nativo ou de modo misto porque os serviços Kerberos não estão disponíveis em domínios de nível inferior.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453500"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitações de autenticação mútua com Kerberos

A conta do cliente e a conta do serviço devem estar em domínios do Windows 2000 nativo ou de modo misto porque os serviços Kerberos não estão disponíveis em domínios de nível inferior. Além disso, as contas de cliente e serviço devem estar na mesma floresta porque o KDC do cliente usa o catálogo global para pesquisar o nome da entidade de serviço.

Tanto o serviço quanto o cliente devem estar em execução no Windows 2000, caso contrário, a autenticação mútua com o Kerberos falhará porque as versões anteriores do Windows não dão suporte ao Kerberos.

Os nomes da entidade de serviço devem incluir o nome DNS do servidor host no qual o serviço está em execução. Você deve usar o nome DNS.

 

 




