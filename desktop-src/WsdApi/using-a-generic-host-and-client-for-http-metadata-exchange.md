---
description: Se o cliente e o host não puderem trocar metadados, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Usando um host genérico e um cliente para metadados HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10040f4834df1a77115a361d23d82ec3dfcc6c57
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883178"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Usando um host genérico e um cliente para metadados HTTP Exchange

Se o cliente e o host não puderem trocar metadados, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema. Se o endereço do dispositivo ou os metadados do dispositivo não aparecerem na saída do cliente de depuração WSD, os endereços de transporte fornecidos ou o ambiente de rede poderão estar causando a falha. Para obter mais informações sobre o host e o cliente genéricos, consulte [ferramentas de depuração](debugging-tools.md).

Se tiver verificado que um host genérico e um cliente podem concluir a troca de metadados WS-Discovery e HTTP, esse procedimento de diagnóstico pode ser ignorado e a solução de problemas pode ser continuada seguindo os procedimentos em [como usar o log do WinHTTP para verificar se há tráfego](using-winhttp-logging-to-verify-get-traffic.md).

Se o host ou o cliente for um aplicativo em execução em um computador, o host ou cliente genérico deverá ser executado no mesmo contexto de segurança que o host ou cliente real. Por exemplo, se o host ou o cliente real for executado como administrador, o host ou cliente genérico deverá ser executado como administrador. Além disso, se o host ou o cliente for um dispositivo autônomo, ele deverá ser completamente substituído por um computador que esteja executando um cliente ou host genérico em um contexto de segurança que garanta acesso ilimitado à rede (por exemplo, executando como administrador).

**Para usar um host genérico e um cliente para solucionar problemas de troca de metadados HTTP**

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

3.  Execute o seguinte comando: **WSDDebug \_client.exe/Mode Metadata/Hello off/resolve** *&lt; ID &gt;*. Substitua *&lt; ID &gt;* pela ID do dispositivo identificada na etapa 2.
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
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

O cliente de depuração WSD pode gerar muita saída em uma rede com muitos dispositivos DPWS. A saída pode ser redirecionada para um arquivo para facilitar a análise. Digite **log t** *&lt; filename &gt;* no prompt do cliente de depuração WSD para redirecionar a saída para um arquivo. O redirecionamento de saída pode ser interrompido digitando o registro de tempo de **interrupção do log** no prompt do cliente de depuração WSD.

Anote o endereço de referência do ponto de extremidade (EPR). Esse endereço de EPR deve corresponder à ID do dispositivo identificada na etapa 2 acima. Além disso, verifique se o cliente de depuração WSD imprimiu completamente os metadados do dispositivo. Os metadados do dispositivo começam com `Metadata for host` e terminam com `End of metadata` .

Se a ID do dispositivo e os metadados do dispositivo aparecerem corretamente na saída do cliente de depuração WSD, a falha do aplicativo provavelmente não estará relacionada aos endereços de transporte fornecidos, ao sistema operacional ou ao ambiente de rede. Substitua o host genérico e o cliente pelo host e cliente personalizados e continue a solução de problemas seguindo os procedimentos em [como usar o log do WinHTTP para verificar o tráfego Get](using-winhttp-logging-to-verify-get-traffic.md).

Se o endereço do dispositivo e os metadados do dispositivo não aparecerem na saída do cliente de depuração WSD, a falha poderá ter uma ou mais das seguintes causas:

-   O endereço de transporte anunciado pelo host está incorreto ou malformado. O cliente de depuração WSD tenta obter os metadados do dispositivo da URL fornecida no elemento **XAddrs** de uma mensagem [ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) . A URL usada para troca de metadados aparece na saída do cliente de depuração WSD, prefixada pela frase `Using xAddr` . O exemplo a seguir mostra o XAddrs usado para troca de metadados na saída do cliente de depuração WSD acima.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Se o XAddrs fornecido não estiver em conformidade com as [regras de validação do XAddr](xaddr-validation-rules.md), o cliente de depuração WSD não poderá obter os metadados do dispositivo.

-   O aplicativo está sendo executado no contexto de segurança incorreto. Verifique se o aplicativo está usando as credenciais corretas e se o cliente e o host têm permissão suficiente para acessar a rede.
-   A configuração do firewall está incorreta. siga as instruções em [inspecionando adaptador e Firewall Configurações](inspecting-adapter-and-firewall-settings.md) para verificar se as configurações de firewall do Windows estão corretas e se não há outras regras descartando os pacotes. O cliente e o host também podem ser copiados em um computador "original" (um com uma instalação padrão do sistema operacional que nunca tenha sido unida a um domínio) para tentar reproduzir a falha.
-   Uma política IPSec está bloqueando o aplicativo. Copie o cliente e o host em um computador que não esteja sujeito a diretivas IPSec e tente reproduzir a falha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



