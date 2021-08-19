---
title: Usando Teredo com o Auxiliar de IP
description: A API do Auxiliar de Protocolo IP é utilizada por um aplicativo para coletar e fornecer informações importantes sobre a configuração de rede do computador local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e977dd585f9759a4eef93daca55e0ff95abdc98085393577afabb4ae6e5908ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990795"
---
# <a name="using-teredo-with-ip-helper"></a>Usando Teredo com o Auxiliar de IP

A API [do](/windows/desktop/IpHlp/about-ip-helper) Auxiliar de Protocolo IP é utilizada por um aplicativo para coletar e fornecer informações importantes sobre a configuração de rede do computador local. Ao operar na plataforma Windows Vista, essas informações incluem a porta UDP dinâmica atribuída à interface Teredo e as alterações que podem ocorrer na porta designada.

As seguintes funções são utilizadas pela API auxiliar de IP para facilitar o uso da interface Teredo:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 