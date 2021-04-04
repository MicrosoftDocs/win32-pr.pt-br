---
title: Substituição de protocolo
description: Substituição de protocolo
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- SDK do Windows Media Format, substituição de protocolo
- ASF (Advanced Systems Format), substituição de protocolo
- ASF (formato de sistemas avançados), substituição de protocolo
- substituição de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007116"
---
# <a name="protocol-rollover"></a>Substituição de protocolo

A substituição de protocolo é um processo pelo qual o objeto leitor descobre o melhor protocolo de streaming disponível de um servidor. O leitor usa a substituição de protocolo sempre que abre uma URL que contém um esquema "MMS".

O leitor dá suporte a vários protocolos:

-   Protocolo RTSP (real time streaming)
-   Protocolo HTTP
-   Microsoft Media Server (MMS)

Os protocolos RTSP e MMS são fornecidos em dois tipos, um usando o [*UDP*](wmformat-glossary.md) como o protocolo de entrega subjacente e o outro usando TCP.

O objeto leitor sempre usa TCP para comandos de controle de reprodução, mas pode usar TCP ou UDP para distribuição do conteúdo transmitido. O UDP é preferencial para a entrega de conteúdo, pois impõe menos sobrecarga de largura de banda do que o TCP. O protocolo TCP garante um transporte confiável por meio do uso de "circuitos virtuais", mas o custo de fazer isso significa que o TCP não é tão adequado para fluxos de mídia digital, em que o uso eficiente da largura de banda é mais importante que os pacotes perdidos ocasionais.

Quando uma URL especifica "mms://", o leitor tenta usar os seguintes protocolos para entrega de dados, na seguinte ordem:

1.  RTSPu (RTSP usando UDP)
2.  RTSPt (RTSP usando TCP)
3.  MMSU (MMS usando UDP)
4.  MMST (MMS usando TCP)
5.  HTTP

HTTP é um protocolo unidirecional baseado em TCP e é o protocolo usado por servidores Web. O streaming com HTTP é menos eficiente que usar RTSP. No entanto, a maioria dos firewalls é configurada para aceitar solicitações HTTP, enquanto elas normalmente rejeitam outros protocolos de streaming.

O Windows Media Services 9 Series no Microsoft Windows Server 2003 rejeitará todas as solicitações de MMSU ou MMST de um leitor do SDK de formato de mídia do Windows, porque o RTSP é o protocolo de streaming preferencial. O Windows Media Services versão 4,1 e anteriores não dão suporte a RTSP. Nesse caso, o objeto leitor volta para MMSU ou HTTP.

A substituição de protocolo não se aplicará se o esquema de URL fornecer um protocolo específico, como "rtspu://" para RTSPu ou "https://" para HTTP. Se o esquema de URL for "rtsp://", o leitor tentará RTSPu e RTSPt, mas não outros.

Depois que o leitor abrir um arquivo, você poderá consultar o protocolo que ele está usando chamando o método [**IWMReaderAdvanced2:: Getprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) no leitor. Enquanto o conteúdo está sendo transmitido ou baixado, esse método retorna o nome assim que o conteúdo é completamente armazenado em cache, o método **Getprotocolname** retorna a cadeia de caracteres "cache".

Para obter os nomes de todos os protocolos do Windows Media Server aos quais o leitor dá suporte, chame o método [**IWMReaderNetworkConfig:: GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) no leitor. Você pode desabilitar um ou mais dos protocolos na lista de sobreposição de protocolo do leitor, usando a interface **IWMReaderNetworkConfig** . Por exemplo, o método [**IWMReaderNetworkConfig:: SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) habilita ou desabilita os protocolos baseados em TCP, e [**IWMReaderNetworkConfig:: SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) habilita ou desabilita os protocolos baseados em UDP. Esses métodos se aplicam somente à substituição de protocolo; os protocolos ainda estarão disponíveis se o esquema de URL contiver um protocolo específico. Normalmente, não há motivo para desabilitar qualquer um dos protocolos usados na substituição de protocolo; Isso pode prejudicar o desempenho. No entanto, pode ser útil para teste.

 

 




