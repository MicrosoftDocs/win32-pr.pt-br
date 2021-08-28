---
description: Este tópico descreve os conceitos de interface de rede de alto nível Windows, incluindo as maneiras como eles podem ser identificados no código e suas propriedades.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfaces de Rede
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: d74c875b579a34464190ca039e0176b8c01bef671b0ea6c24581023a49988645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825447"
---
# <a name="network-interfaces"></a>Interfaces de rede

Este tópico descreve os conceitos de interface de rede de alto nível Windows, incluindo as maneiras como eles podem ser identificados no código e suas propriedades. 

> [!IMPORTANT]
> Este tópico destina-se a um público-alvo do desenvolvedor, tanto para aplicativos Windows de rede da área de trabalho quanto drivers de rede de modo kernel. No entanto, algumas das informações apresentadas aqui também podem ser úteis para administradores de sistema que gerenciam interfaces de rede por meio de cmdlets do PowerShell.

## <a name="overview"></a>Visão geral

Um *interface de rede* é o ponto em que duas partes de equipamentos de rede ou camadas de protocolo se conectam. Normalmente, isso é representado por uma NIC (Placa de Interface de Rede) física para conexão entre um computador e uma rede privada ou pública. No entanto, ele também pode assumir a forma de um componente somente de software, como a interface de loopback ( para `127.0.0.1` IPv4 ou `::1` para IPv6).

As interfaces de rede são definidas pela IETF (Internet Engineering Task Force) no [RFC 2863](https://tools.ietf.org/html/rfc2863) e não devem ser definidas por Windows. Para perguntas detalhadas sobre o significado de identificadores de interface de rede, como **ifIndex,** consulte as definições do IETF sobre eles. O restante deste tópico aborda Windows de implementação específicas.

## <a name="network-interface-identifiers-and-properties"></a>Propriedades e identificadores de interface de rede

No Windows, um interface de rede pode ser identificado de maneiras diferentes. Alguns desses identificadores são usados para distinguir interfaces de rede uns dos outros, mas nem todos os identificadores são igualmente adequados para essa tarefa devido a suas propriedades diferentes. Em geral, as interfaces de rede são identificadas por um endereço de rede para componentes externos. Por exemplo, pode ser uma ID de nó e um número da porta ou simplesmente uma ID de nó exclusiva. 

No código, um interface de rede pode ser identificado de várias maneiras. A tabela a seguir detalha as maneiras como um interface de rede pode ser identificado junto com as propriedades associadas. É recomendável usar o GUID da interface (**ifGuid**) para programação, a menos que uma API específica exija um identificador de interface de rede diferente.

> [!NOTE]
> Na tabela a seguir, as células **em negrito** representam uma propriedade desejável para programadores de rede.

| Identificador | Tamanho | É exclusivo no sistema | É exclusivo no mundo | É previsível | Será reciclado se a NIC for removida | Persiste entre reinicializações | Os usuários finais podem modificar a qualquer momento | Os drivers podem ser modificados a qualquer momento | Familiaridade geral com os usuários finais | Está sempre presente |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Se_índice** | **4 bytes** | **Sim** | Não | Não | Sim | Não<sup>1</sup> | **Não** | **Não** | **Alguns**<sup>2</sup> | **Sim** |
| **NetLuid** | **8 bytes** | **Sim** | Não | Não | Sim | **Sim** | **Não** | **Não** | Não | **Sim** |
| **ifGuid** | **16 bytes** | **Sim** | **Normalmente,**<sup>3</sup> | Não | **Não** | **Sim** | **Não** | **Não** | Não | **Sim** |
| **ifAlias** | 514 bytes | **Sim para NICs**<sup>4</sup> | Não | Às<sup>vezes, 5</sup> | Sim | **Sim** | Sim | **Não** | **Sim** | **Normalmente,**<sup>4</sup> |
| **ifDescr** | 514 bytes | Normalmente,<sup>6</sup> | Não | Não | Sim | **Sim** | **Não** | Sim | **Sim** | **Geralmente** |
| **ifPhysAddress (ENDEREÇO MAC)**| 0 a 32 bytes | Normalmente, para NICs | **Normalmente, para NICs** | **Sim** | **Vinculado ao hardware** | **Sim** | **Não** | **Não** | **Sim** | **Normalmente,** <sup>7</sup> |
| **ID da instância pnP** | Até 400 bytes | **Sim** | Não | Não | Sim | **Sim** | **Não** | **Não** | Não | **Normalmente, para NICs**<sup>8</sup> |
| **Local do PnP (número do slot PCI)** | Até 400 bytes | **Sim** | Não | **Sim** | Sim | **Sim** | **Não** | **Não** | Às vezes | Às<sup>vezes, 8,9</sup> |

Observações para a tabela anterior:

1. **Não há garantia de que IfIndexes** seja estável entre reinicializações, mesmo que geralmente recebam o mesmo valor da inicialização anterior. Portanto, não é recomendável que os drivers **usem ifIndex,** exceto quando exigido por uma API.
2. Alguns `netsh` comandos levam , ou , como uma `ifIndex` `index` entrada. Portanto, alguns usuários administrativos estão familiarizados com a **propriedade ifIndex** se usarem `netsh` o comando com frequência.
3. Se um computador for clonado ou tiver imagens, alguns dos GUIDs poderão ser os mesmos. Além disso, determinadas interfaces de rede especiais, como a interface Teredo interna, podem ter o mesmo GUID em todos os máquinas.
4. O NetCfg impõe que um **ifAlias** seja uma cadeia de caracteres não vazia e seja exclusivo entre todas as NICs. No entanto, o provedor de interface NDIS não faz isso. Assim, é possível encontrar interfaces de rede especiais com nomes duplicados ou vazios. Isso é mais comumente visto com equipes lbFO.
5. Somente se o firmware for compatível com Nomen entre dispositivos consistentes. Tipicamente, os servidores têm esse recurso.
6. O NetCfg atribui **ifDescrs exclusivo a** todos os interfaces de rede. No entanto, os drivers podem chamar uma API para alterar **o ifDescr** para qualquer coisa, incluindo algo que não é exclusivo. Alguns pacotes de software de terceiros fazem isso.
7. Nem todos os tipos de mídia têm um "endereço MAC". Por exemplo, alguns túneis não têm esse conceito e simplesmente anunciam uma matriz de byte de comprimento zero como seu endereço de rede.
8. Presente apenas em interfaces de rede que têm o suporte de um dispositivo PnP. Por exemplo, interfaces de loopback, interfaces de filtro de peso leve, interfaces fornecidas por um provedor de interface NDIS e determinadas NICs especiais integrados não têm dispositivos PnP que as têm como base.
9. Somente alguns caminhões PnP são suportados por uma ID de local do PnP. Os caminhões PCI e USB integrados fazem isso, enquanto os dispositivos enumerados por raiz não.

## <a name="visibility-to-developers"></a>Visibilidade para desenvolvedores

Na tabela anterior, todas as propriedades, exceto as propriedades Plug and Play (PnP), são visíveis para aplicativos da área de trabalho do modo de usuário e drivers de modo kernel por meio de um header compartilhado (Netioapi.h). As propriedades pnP são visíveis por meio do header Devpkey.h e são usadas por aplicativos da área de trabalho do modo de usuário e drivers de modo kernel. Por exemplo, consulte a [documentação de DEVPKEY.](/windows-hardware/drivers/install/devpkey-device-instanceid)

A [API auxiliar de IP](/windows/desktop/IpHlp/ip-helper-start-page) também está disponível para aplicativos da área de trabalho do modo de usuário e drivers de modo kernel.

A superfície da API UWP expõe apenas a [propriedade ifGuid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) diretamente. No entanto, é possível que os desenvolvedores de aplicativos UWP importem a função [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) usando P/Invoke se eles são necessários para acessar outras propriedades de interface de rede.

## <a name="related-topics"></a>Tópicos relacionados

Para definições de MIB (base de informações de gerenciamento) para interfaces de rede, [consulte RFC 2863](https://tools.ietf.org/html/rfc2863).

Para interfaces de rede NDIS em drivers de rede, consulte [Interfaces de rede NDIS](/windows-hardware/drivers/network/ndis-network-interfaces2).

Para referência de API netioapi.h, consulte [o header netioapi.h](/windows/desktop/api/netioapi/).
