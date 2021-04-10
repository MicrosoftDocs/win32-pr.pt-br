---
description: Computadores pessoais que executam o Microsoft Windows geralmente têm várias conexões de rede, como várias placas de interface de rede (NIC) conectadas a redes diferentes, ou uma conexão de rede física e uma conexão dial-up.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Provedor de serviços de reconhecimento de local de rede (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090368"
---
# <a name="network-location-awareness-service-provider-nla"></a>Provedor de serviços de reconhecimento de local de rede (NLA)

Computadores pessoais que executam o Microsoft Windows geralmente têm várias conexões de rede, como várias placas de interface de rede (NIC) conectadas a redes diferentes, ou uma conexão de rede física e uma conexão dial-up. O Windows Sockets foi capaz de enumerar as interfaces de rede disponíveis por algum tempo, mas algumas informações críticas sobre as conexões de rede estavam indisponíveis anteriormente. Isso inclui informações como a rede lógica à qual um computador Windows está conectado ou se várias interfaces estão conectadas à mesma rede.

O provedor de serviços de reconhecimento de local de rede, conhecido como NLA, permite que aplicativos Windows Sockets 2 identifiquem a rede lógica à qual um computador Windows está conectado. Além disso, o NLA permite que os aplicativos Windows Sockets identifiquem em qual interface de rede física um determinado aplicativo salvou informações específicas. O NLA é implementado como um provedor de serviço de resolução de nomes do Windows Sockets 2 genérico.

 

 



