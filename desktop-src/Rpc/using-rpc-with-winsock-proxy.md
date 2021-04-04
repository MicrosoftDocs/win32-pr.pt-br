---
title: Usando RPC com proxy Winsock
description: Usando RPC com proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008321"
---
# <a name="using-rpc-with-winsock-proxy"></a>Usando RPC com proxy Winsock

O lançamento do Microsoft Internet Access Server incluiu o proxy Winsock, uma versão aprimorada da API do Windows Sockets versão 1,1. O proxy Winsock permite que um aplicativo Windows Sockets, em execução em um cliente de rede privada, se comporte como se estivesse conectado diretamente a um aplicativo de servidor de Internet remoto. O servidor proxy da Microsoft atua como o host para essa conexão. Isso significa que todas as comunicações no nível do aplicativo são canalizadas por meio de um único computador protegido – o computador de gateway que executa o Microsoft Proxy Server.

Normalmente, para transferências de pacote de datagrama, a DLL de transporte RPC ignora as funções [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) fornecidas no Wsock32.dll e se comunica diretamente com o driver de dispositivo subjacente. Isso melhora a velocidade das transferências de pacote, mas torna os recursos de proxy Winsock indisponíveis para o aplicativo.

Cada provedor de protocolo de rede tem um GUID associado. A biblioteca de tempo de execução RPC compara os GUIDs UDP e IPX com os identificadores bem conhecidos da Microsoft. Se eles não corresponderem, o RPC usará automaticamente o Winsock.

Outro recurso do proxy Winsock é sua capacidade de emular o protocolo de transporte TCP no transporte do Novell SPX quando o computador cliente SPX não tiver o TCP instalado. Para usar esse recurso com aplicativos RPC, edite o registro do sistema em cada computador cliente para adicionar essa entrada:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Edite o registro em cada computador do servidor para adicionar esta entrada:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Para obter mais informações sobre protocolos de transporte RPC, consulte [especificando sequências de protocolo](specifying-protocol-sequences.md). Para obter mais informações sobre o proxy Winsock, consulte a documentação do produto para o Microsoft Internet Access Server.

O Windows 2000 não implementa as entradas do registro **ClientProtocols** e **ServerProtocols** . A Microsoft fornece todos os transportes bem conhecidos como parte da biblioteca de tempo de execução. Portanto, essas entradas não são necessárias.

 

 