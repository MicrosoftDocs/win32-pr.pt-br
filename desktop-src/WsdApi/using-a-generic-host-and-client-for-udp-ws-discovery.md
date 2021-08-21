---
description: Se o cliente e o host não puderem ver uns aos outros na rede, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Usando um host genérico e um cliente para UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6af77529116e21848e22812e04322273e08f1f0cf4d107787b4039b2442b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991486"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Usando um host genérico e um cliente para UDP WS-Discovery

Se o cliente e o host não puderem ver uns aos outros na rede, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema. Se o endereço do dispositivo não aparecer na saída do cliente de depuração WSD, o ambiente de rede provavelmente está causando a falha. Para obter mais informações sobre o host e o cliente genéricos, consulte [ferramentas de depuração](debugging-tools.md).

Se o host ou o cliente for um aplicativo em execução em um computador, o host ou cliente genérico deverá ser executado no mesmo contexto de segurança que o host ou cliente real. Por exemplo, se o host ou o cliente real for executado como administrador, o host ou cliente genérico deverá ser executado como administrador. Além disso, se o host ou o cliente for um dispositivo autônomo, ele deverá ser completamente substituído por um computador que esteja executando um cliente ou host genérico.

**Para usar um host genérico e um cliente para solucionar problemas de descoberta de WS-Discovery**

1.  Abra uma janela de prompt de comando.
2.  Execute o seguinte comando: **WSDDebug \_host.exe/Mode Metadata/Start**

    > [!Note]  
    > uma caixa de diálogo **Segurança do Windows alerta** pode ser exibida. Nesse caso, clique em **desbloquear** para permitir que o host de depuração WSD seja executado.

     

    Esse comando gera uma saída semelhante à seguinte. Anote a ID do dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Execute o seguinte comando: **WSDDebug \_client.exe/Mode Metadata/Hello off/resolve** *<id>* . Substitua *<id>* pela ID do dispositivo identificada na etapa 2.
    > [!Note]  
    > uma caixa de diálogo **Segurança do Windows alerta** pode ser exibida. Nesse caso, clique em **desbloquear** para permitir que o cliente de depuração WSD seja executado.

     

O cliente de depuração WSD gera uma saída semelhante à seguinte.

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

O cliente de depuração WSD pode gerar muita saída em uma rede com muitos dispositivos DPWS. A saída pode ser redirecionada para um arquivo para facilitar a análise. Digite o arquivo de **log** de texto *<filename>* no prompt do cliente de depuração WSD para redirecionar a saída para um arquivo. O redirecionamento de saída pode ser interrompido digitando o registro de tempo de **interrupção do log** no prompt do cliente de depuração WSD.

Anote o endereço de referência do ponto de extremidade (EPR). Esse endereço de EPR deve corresponder à ID do dispositivo identificada na etapa 2 acima. Se esse for o caso, a falha do aplicativo provavelmente não estará relacionada ao sistema operacional ou ao ambiente de rede. Substitua o host genérico e o cliente pelo host e cliente personalizados e continue a solução de problemas seguindo os procedimentos em [usando o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).

Se a ID do dispositivo não corresponder ao endereço EPR, a falha do aplicativo provavelmente estará relacionada ao sistema operacional ou ao ambiente de rede. A falha pode ter uma ou mais das seguintes causas:

-   O aplicativo está sendo executado no contexto de segurança incorreto. Verifique se o aplicativo está usando as credenciais corretas e se o cliente e o host têm permissão suficiente para acessar a rede.
-   A configuração do firewall está incorreta. siga as instruções em [inspecionando adaptador e Firewall Configurações](inspecting-adapter-and-firewall-settings.md) para verificar se as configurações de firewall do Windows estão corretas e se não há outras regras descartando os pacotes. O cliente e o host também podem ser copiados em um computador "original" (um com uma instalação padrão do sistema operacional que nunca tenha sido unida a um domínio) para tentar reproduzir a falha.
-   Uma política IPSec está bloqueando o aplicativo. Copie o cliente e o host em um computador que não esteja sujeito a diretivas IPSec e tente reproduzir a falha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



