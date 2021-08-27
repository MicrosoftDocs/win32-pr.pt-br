---
description: Se o cliente e o host não puderem se ver na rede, um host genérico e um cliente poderão ser substituídos pelo host personalizado e pelo cliente para ajudar a solucionar o problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Usando um host genérico e um cliente para UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b9f42cd76e54c3ee04a3299e9f23eecbfdd73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883074"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Usando um host genérico e um cliente para UDP WS-Discovery

Se o cliente e o host não puderem se ver na rede, um host genérico e um cliente poderão ser substituídos pelo host personalizado e pelo cliente para ajudar a solucionar o problema. Se o endereço do dispositivo não aparecer na saída do cliente de depuração do WSD, o ambiente de rede provavelmente está causando a falha. Para obter mais informações sobre o host genérico e o cliente, consulte [Ferramentas de depuração](debugging-tools.md).

Se o host ou o cliente for um aplicativo em execução em um computador, o host genérico ou o cliente deverá ser executado no mesmo contexto de segurança que o host ou o cliente real. Por exemplo, se o host ou cliente real for executado como Administrador, o host genérico ou o cliente deverá ser executado como Administrador. Além disso, se o host ou o cliente for um dispositivo autônomo, ele deverá ser completamente substituído por um computador que executa um host ou cliente genérico.

**Para usar um host genérico e um cliente para solucionar problemas de WS-Discovery UDP**

1.  Abra uma janela de prompt de comando.
2.  Execute o seguinte comando: **WSDDebughost.exe \_ /mode metadata /start**

    > [!Note]  
    > Uma **Segurança do Windows caixa de diálogo Alerta** pode aparecer. Em caso afirmatório, **clique em Desbloquear** para permitir que o Host de Depuração do WSD seja executado.

     

    Esse comando gera uma saída semelhante à seguinte. Anote a ID do dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Execute o seguinte comando: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *&lt; id &gt;*. Substitua *&lt; id &gt;* pela ID do dispositivo identificada na etapa 2.
    > [!Note]  
    > Uma **Segurança do Windows caixa de diálogo Alerta** pode aparecer. Em caso afirmatório, **clique em Desbloquear** para permitir que o Cliente de Depuração do WSD seja executado.

     

O cliente de depuração do WSD gera uma saída semelhante à seguinte.

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
```

O cliente de depuração do WSD pode gerar muita saída em uma rede com muitos dispositivos DPWS. A saída pode ser redirecionada para um arquivo para uma análise mais fácil. Digite **log tee** *&lt; &gt; filename no* prompt do cliente de depuração do WSD para redirecionar a saída para um arquivo. O redirecionamento de saída pode ser interrompido digitando **log no** prompt do Cliente de Depuração do WSD.

Anote o endereço de EPR (referência de ponto de extremidade). Esse endereço de EPR deve corresponder à ID do dispositivo identificada na etapa 2 acima. Se esse for o caso, a falha do aplicativo provavelmente não está relacionada ao sistema operacional ou ao ambiente de rede. Substitua o host genérico e o cliente pelo host personalizado e pelo cliente e continue a solução de problemas seguindo os procedimentos em Usando o cliente de depuração do WSD para verificar o tráfego [multicast.](using-wsddebug-client-to-verify-multicast-traffic.md)

Se a ID do dispositivo não corresponder ao endereço EPR, a falha do aplicativo provavelmente está relacionada ao sistema operacional ou ao ambiente de rede. A falha pode ter uma ou mais das seguintes causas:

-   O aplicativo está em execução no contexto de segurança errado. Verifique se o aplicativo está usando as credenciais corretas e se o cliente e o host têm permissão suficiente para acessar a rede.
-   A configuração do firewall está errada. Siga as instruções em [Inspecionando](inspecting-adapter-and-firewall-settings.md) o adaptador e Configurações firewall para verificar se as configurações Windows Firewall do Windows estão corretas e se não há outras regras descartando os pacotes. O cliente e o host também podem ser copiados em um computador "pristine" (um com uma instalação de sistema operacional padrão que nunca foi ingressada em um domínio) para tentar reproduzir a falha.
-   Uma política de IPSec está bloqueando o aplicativo. Copie o cliente e o host em um computador não sujeito a políticas IPSec e tente reproduzir a falha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



