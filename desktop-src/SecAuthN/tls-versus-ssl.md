---
description: O TLS é um padrão bem relacionado ao SSL 3,0 e, às vezes, é chamado de &\# 0034; SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS vs. SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748409"
---
# <a name="tls-vs-ssl"></a>TLS vs. SSL

O TLS é um padrão bem relacionado ao SSL 3,0 e, às vezes, é chamado de "SSL 3,1". O TLS substitui o SSL 2,0 e deve ser usado em um novo desenvolvimento. A partir do Windows 10, versão 1607 e Windows Server 2016, o SSL 2,0 foi removido e não tem mais suporte.

Os aplicativos que exigem um alto nível de interoperabilidade devem dar suporte a SSL 3,0 e TLS. Devido às semelhanças entre esses dois protocolos, os detalhes de SSL não são incluídos nesta documentação, exceto onde diferem do TLS. O seguinte é do [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):

"As diferenças entre esse protocolo e o SSL 3,0 não são dramáticas, mas são significativas o suficiente para que o TLS 1,0 e o SSL 3,0 não interoperem (embora o TLS 1,0 incorpore um mecanismo pelo qual uma implementação de TLS possa fazer o backup para SSL 3,0)."

 

 



