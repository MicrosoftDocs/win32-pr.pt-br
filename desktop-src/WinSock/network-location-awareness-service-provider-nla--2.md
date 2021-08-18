---
description: Computadores pessoais que executam o Microsoft Windows geralmente têm várias conexões de rede, como várias NIC (placas de interface de rede) conectadas a redes diferentes, ou uma conexão de rede física e uma conexão discar.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: NLA (Provedor de Serviços de Reconhecimento de Localização de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7378aff6f51f2785671f1d424a4721f9cd77fad22d60554746f9427d7f24f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132089"
---
# <a name="network-location-awareness-service-provider-nla"></a>NLA (Provedor de Serviços de Reconhecimento de Localização de Rede)

Computadores pessoais que executam o Microsoft Windows geralmente têm várias conexões de rede, como várias NIC (placas de interface de rede) conectadas a redes diferentes, ou uma conexão de rede física e uma conexão discar. Windows Os soquetes têm sido capazes de enumerar adaptadores de rede disponíveis há algum tempo, mas determinadas informações críticas sobre conexões de rede anteriormente não estavam disponíveis. Isso inclui informações como a rede lógica à qual um computador Windows está anexado ou se várias interfaces estão conectadas à mesma rede.

O provedor de serviços de Reconhecimento de Localização de Rede, conhecido como NLA, permite que os aplicativos Windows Sockets 2 identifiquem a rede lógica à qual um computador Windows está anexado. Além disso, o NLA permite Windows soquetes para identificar para qual interface de rede física um determinado aplicativo salvou informações específicas. O NLA é implementado como um provedor de serviços Windows de resolução de nomes soquetes 2 genéricos.

 

 



