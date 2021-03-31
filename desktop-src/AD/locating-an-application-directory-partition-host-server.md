---
title: Localizando um servidor de host de partição de diretório de aplicativo
description: Este tópico descreve como localizar um servidor de host de partição de diretório de aplicativo.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Localizando um servidor host de partição de diretório de aplicativo AD
- AD de partições de diretório de aplicativo, localizando um servidor host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634937"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Localizando um servidor de host de partição de diretório de aplicativo

O serviço NetLogon registra a seguinte lista de registros SRV para uma partição de diretório de aplicativo:

-   \_LDAP. \_ Protocol.<partition name>
-   \_LDAP. \_ TCP. <site name> . \_ sites.<partition name>

Para localizar um controlador de domínio que hospede uma réplica de uma partição de diretório de aplicativo especificada, chame a função [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) com o parâmetro *DomainName* definido como o nome DNS da partição de diretório de aplicativo e o sinalizador **\_ somente \_ LDAP \_ necessário** definido no parâmetro *flags* . Para obter mais informações e um exemplo de código que mostra, usando a função **DsGetDcName** , como localizar um controlador de domínio que hospeda uma réplica de uma partição de diretório de aplicativos, consulte [código de exemplo para localizar um servidor de host de partição de diretório de aplicativo](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




