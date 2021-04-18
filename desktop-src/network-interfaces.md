---
description: Este tópico descreve os conceitos de interface de rede de alto nível no Windows, incluindo as maneiras que eles podem ser identificados no código e suas propriedades.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfaces de Rede
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: cc31be6062469750049a676807c2f8da24f473f1
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105764068"
---
# <a name="network-interfaces"></a>Interfaces de rede

Este tópico descreve os conceitos de interface de rede de alto nível no Windows, incluindo as maneiras que eles podem ser identificados no código e suas propriedades. 

> [!IMPORTANT]
> Este tópico destina-se a um público de desenvolvedor, para aplicativos de rede de área de trabalho do Windows e drivers de rede de modo kernel. No entanto, algumas das informações apresentadas aqui também podem ser úteis para administradores de sistema que gerenciam interfaces de rede por meio de cmdlets do PowerShell.

## <a name="overview"></a>Visão geral

Uma *interface de rede* é o ponto em que duas partes do equipamento de rede ou camadas de protocolo se conectam. Normalmente, isso é representado por uma NIC (placa de interface de rede) física para conexão entre um computador e uma rede privada ou pública. No entanto, ele também pode assumir a forma de um componente somente de software, como a interface de loopback ( `127.0.0.1` para IPv4 ou `::1` IPv6).

As interfaces de rede são definidas pelo IETF (Internet Engineering Task Force) no [RFC 2863](https://tools.ietf.org/html/rfc2863) e não devem ser definidas pelo Windows. Para obter perguntas detalhadas sobre o significado dos identificadores de interface de rede, como **ifIndex**, consulte as definições da IETF deles. O restante deste tópico discute detalhes de implementação específicos do Windows.

## <a name="network-interface-identifiers-and-properties"></a>Identificadores e propriedades de interface de rede

No Windows, uma interface de rede pode ser identificada de maneiras diferentes. Alguns desses identificadores são usados para distinguir adaptadores de rede uns dos outros, mas nem todos os identificadores são igualmente adequados para essa tarefa devido a suas propriedades diferentes. Geralmente, as interfaces de rede são identificadas por um endereço de rede para componentes externos. Por exemplo, isso pode ser uma ID de nó e um número de porta, ou simplesmente uma ID de nó exclusiva. 

No código, uma interface de rede pode ser identificada de várias maneiras. A tabela a seguir detalha as maneiras como um adaptador de rede pode ser identificado junto com as propriedades associadas. É recomendável usar o GUID de interface (**ifGuid**) para a programação, a menos que uma API específica exija um identificador de interface de rede diferente.

> [!NOTE]
> Na tabela a seguir, as células em **negrito** representam uma propriedade que é desejável para programadores de rede.

| Identificador | Tamanho | É exclusivo no sistema | É exclusivo no mundo | É previsível | Será reciclado se a NIC for removida | Persiste entre reinicializações | Os usuários finais podem modificar a qualquer momento | Os drivers podem ser modificados a qualquer momento | Familiaridade geral com os usuários finais | Está sempre presente |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 bytes** | **Sim** | Não | Não | Sim | Não<sup>1</sup> | **Não** | **Não** | **Alguns**<sup>2</sup> | **Sim** |
| **NetLuid** | **8 bytes** | **Sim** | Não | Não | Sim | **Sim** | **Não** | **Não** | Não | **Sim** |
| **ifGuid** | **16 bytes** | **Sim** | **Geralmente**<sup>3</sup> | No | **Não** | **Sim** | **Não** | **Não** | Não | **Sim** |
| **ifAlias** | 514 bytes | **Sim para NICs**<sup>4</sup> | No | Às vezes<sup>5</sup> | Sim | **Sim** | Sim | **Não** | **Sim** | **Geralmente**<sup>4</sup> |
| **ifDescr** | 514 bytes | Geralmente<sup>6</sup> | Não | Não | Sim | **Sim** | **Não** | Sim | **Sim** | **Refere** |
| **ifPhysAddress (endereço MAC)**| 0 a 32 bytes | Geralmente, para NICs | **Geralmente, para NICs** | **Sim** | **Vinculado ao hardware** | **Sim** | **Não** | **Não** | **Sim** | **Geralmente** <sup>7</sup> |
| **ID da instância PnP** | Até 400 bytes | **Sim** | Não | Não | Sim | **Sim** | **Não** | **Não** | No | **Geralmente, para NICs**<sup>8</sup> |
| **Localização de PnP (número de slot PCI)** | Até 400 bytes | **Sim** | Não | **Sim** | Sim | **Sim** | **Não** | **Não** | Casos | Às vezes<sup>, 8, 9</sup> |

Observações para a tabela anterior:

1. Não há garantia de que o **IfIndexes** seja estável entre as reinicializações, mesmo que elas recebam o mesmo valor da inicialização anterior. Portanto, não é recomendável que os drivers usem **ifIndex** , exceto quando exigido por uma API.
2. Alguns `netsh` comandos levam `ifIndex` ou `index` , como uma entrada. Portanto, alguns usuários administrativos estarão familiarizados com a propriedade **ifIndex** se usarem o `netsh` comando com frequência.
3. Se um computador for clonado ou tiver uma imagem, alguns dos GUIDs poderão ser iguais. Além disso, determinadas interfaces de rede especiais, como a interface teredo interna, podem ter o mesmo GUID em todos os computadores.
4. O NetCfg impõe que um **ifAlias** seja uma cadeia de caracteres não vazia e seja exclusivo entre todas as NICs. No entanto, o provedor de interface NDIS não faz isso. Cuidamos, é possível encontrar interfaces de rede especiais com nomes duplicados ou vazios. Isso é mais comumente visto com as equipes do LBFO.
5. Somente se o firmware oferecer suporte a nomes de dispositivo consistentes. Typcically, os servidores têm esse recurso.
6. O NetCfg atribui **ifDescrs** exclusivas a todas as interfaces de rede. No entanto, os drivers podem chamar uma API para alterar o **ifDescr** para qualquer coisa, incluindo algo que não seja exclusivo. Alguns pacotes de software de terceiros fazem isso.
7. Nem todos os tipos de mídia têm um "endereço MAC". Por exemplo, alguns túneis não têm esse conceito e simplesmente anunciam uma matriz de bytes de comprimento zero como seu endereço de rede.
8. Presente apenas em interfaces de rede que são apoiadas por um dispositivo PnP. Por exemplo, interfaces de loopback, interfaces de filtro de peso leve, interfaces fornecidas por um provedor de interface NDIS e determinadas NICs internas especiais não têm dispositivos PnP fazendo backup deles.
9. Somente alguns barramentos PnP dão suporte a uma ID de local PnP. Os barramentos PCI e USB internos têm, enquanto os dispositivos enumerados por raiz não têm.

## <a name="visibility-to-developers"></a>Visibilidade para desenvolvedores

Na tabela anterior, todas as propriedades, exceto as propriedades de Plug and Play (PnP), são visíveis para aplicativos de área de trabalho de modo de usuário e drivers de modo kernel por meio de um cabeçalho compartilhado (Netioapi. h). As propriedades PnP são visíveis por meio do cabeçalho Devpkey. h e são usadas por aplicativos de área de trabalho de modo de usuário e drivers de modo kernel. Por exemplo, consulte a documentação do [DEVPKEY](/windows-hardware/drivers/install/devpkey-device-instanceid) .

A API [auxiliar de IP](/windows/desktop/IpHlp/ip-helper-start-page) também está disponível para aplicativos de área de trabalho de modo de usuário e drivers de modo kernel.

A superfície da API UWP expõe apenas a propriedade [ifGuid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) diretamente. No entanto, é possível que os desenvolvedores de aplicativos UWP importem a função [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) usando P/Invoke se forem necessários para acessar outras propriedades de interface de rede.

## <a name="related-topics"></a>Tópicos relacionados

Para definições de MIB (base de informações de gerenciamento) para interfaces de rede, consulte [RFC 2863](https://tools.ietf.org/html/rfc2863).

Para interfaces de rede NDIS em drivers de rede, consulte [interfaces de rede NDIS](/windows-hardware/drivers/network/ndis-network-interfaces2).

Para referência de API Netioapi. h, consulte o [cabeçalho Netioapi. h](/windows/desktop/api/netioapi/).
