---
title: Usando Teredo com auxiliar de IP
description: A API do auxiliar de protocolo de Internet (IP Helper) é utilizada por um aplicativo para coletar e fornecer informações importantes sobre a configuração de rede do computador local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641394"
---
# <a name="using-teredo-with-ip-helper"></a>Usando Teredo com auxiliar de IP

A API do auxiliar de [protocolo de Internet](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) é utilizada por um aplicativo para coletar e fornecer informações importantes sobre a configuração de rede do computador local. Ao operar na plataforma Windows Vista, essas informações incluem a porta UDP dinâmica atribuída à interface Teredo e as alterações que podem ocorrer na porta designada.

As funções a seguir são utilizadas pela API do auxiliar de IP para facilitar o uso da interface Teredo:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 