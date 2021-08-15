---
title: Localizando um servidor host de partição do diretório de aplicativos
description: Este tópico descreve como localizar um servidor host de partição de diretório do aplicativo.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Localizando um AD do servidor host de partição do diretório de aplicativos
- AD de partições do Diretório do Aplicativo, localizando um servidor host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186787"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Localizando um servidor host de partição do diretório de aplicativos

O serviço NetLogon registra a seguinte lista de registros SRV para uma partição de diretório do aplicativo:

-   \_ldap. \_ Tcp.<partition name>
-   \_ldap. \_ tcp. <site name> . \_ Sites.<partition name>

Para localizar um controlador de domínio que hospeda uma réplica de uma partição de diretório de aplicativo especificada, chame a função [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) com o parâmetro *DomainName* definido como o nome DNS da partição de diretório do aplicativo e o sinalizador **DS \_ ONLY \_ LDAP \_ NEEDED** definido no parâmetro *Flags.* Para obter mais informações e um exemplo de código que mostra, usando a função **DsGetDcName,** como localizar um controlador de domínio que hospeda uma réplica de uma partição de diretório do aplicativo, consulte Código de exemplo para localizar um servidor host de partição do diretório do [aplicativo.](example-code-for-locating-an-application-directory-partition-host-server.md)

 

 




