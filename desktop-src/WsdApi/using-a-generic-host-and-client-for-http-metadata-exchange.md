---
description: Se o cliente e o host não puderem trocar metadados, um host genérico e um cliente poderão ser substituídos pelo host personalizado e pelo cliente para ajudar a solucionar o problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Usando um host genérico e um cliente para metadados HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6623b39989b613e725fb2103165c825425f20b53a4375d6791aa92cd3b99187
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030076"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Usando um host genérico e um cliente para metadados HTTP Exchange

Se o cliente e o host não puderem trocar metadados, um host genérico e um cliente poderão ser substituídos pelo host personalizado e pelo cliente para ajudar a solucionar o problema. Se o endereço do dispositivo ou os metadados do dispositivo não aparecerem na saída do cliente de depuração do WSD, os endereços de transporte fornecidos ou o ambiente de rede poderão estar causando a falha. Para obter mais informações sobre o host genérico e o cliente, consulte [Ferramentas de depuração](debugging-tools.md).

Se tiver sido verificado que um host genérico e um cliente podem concluir a troca de metadados WS-Discovery e HTTP, esse procedimento de diagnóstico poderá ser ignorado e a solução de problemas poderá ser continuada seguindo os procedimentos em Usando o registro em log [do WinHTTP](using-winhttp-logging-to-verify-get-traffic.md)para verificar obter tráfego.

Se o host ou o cliente for um aplicativo em execução em um computador, o host genérico ou o cliente deverá ser executado no mesmo contexto de segurança que o host ou o cliente real. Por exemplo, se o host ou cliente real for executado como Administrador, o host genérico ou o cliente deverá ser executado como Administrador. Além disso, se o host ou o cliente for um dispositivo autônomo, ele deverá ser completamente substituído por um computador que executa um host ou cliente genérico em um contexto de segurança que garanta acesso ilimitado à rede (por exemplo, em execução como Administrador).

**Para usar um host genérico e um cliente para solucionar problemas de troca de metadados HTTP**

1.  Abra uma janela de prompt de comando.
2.  Execute o seguinte comando: **WSDDebughost.exe \_ /mode metadata /start**

    > [!Note]  
    > Uma **Segurança do Windows caixa de diálogo** Alerta pode aparecer. Em caso afirmatório, **clique em Desbloquear** para permitir que o Host de Depuração do WSD seja executado.

     

    Esse comando gera uma saída semelhante à seguinte. Anote a ID do dispositivo.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Execute o seguinte comando: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *<id>* . Substitua *<id>* pela ID do dispositivo identificada na etapa 2.
    > [!Note]  
    > Uma **Segurança do Windows caixa de diálogo** Alerta pode aparecer. Em caso afirmatório, **clique em Desbloquear** para permitir que o Cliente de Depuração do WSD seja executado.

     

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

O cliente de depuração do WSD pode gerar muita saída em uma rede com muitos dispositivos DPWS. A saída pode ser redirecionada para um arquivo para uma análise mais fácil. Digite **log no** prompt do Cliente de Depuração do *<filename>* WSD para redirecionar a saída para um arquivo. O redirecionamento de saída pode ser interrompido digitando **log no** prompt do Cliente de Depuração do WSD.

Anote o endereço de EPR (referência de ponto de extremidade). Esse endereço de EPR deve corresponder à ID do dispositivo identificada na etapa 2 acima. Além disso, verifique se o cliente de depuração do WSD imprimiu completamente os metadados do dispositivo. Os metadados do dispositivo começam com `Metadata for host` e terminam com `End of metadata` .

Se a ID do dispositivo e os metadados do dispositivo aparecerem corretamente na saída do cliente de depuração do WSD, a falha do aplicativo provavelmente não está relacionada aos endereços de transporte fornecidos, ao sistema operacional ou ao ambiente de rede. Substitua o host genérico e o cliente pelo host personalizado e pelo cliente e continue a solução de problemas seguindo os procedimentos em Usando o registro em log [do WinHTTP](using-winhttp-logging-to-verify-get-traffic.md)para verificar obter tráfego.

Se o endereço do dispositivo e os metadados do dispositivo não aparecerem na saída do cliente de depuração do WSD, a falha poderá ter uma ou mais das seguintes causas:

-   O endereço de transporte anunciado pelo host está incorreto ou malformado. O cliente de depuração do WSD tenta obter metadados de dispositivo da URL fornecida no **elemento XAddrs** de uma [mensagem ProbeMatches](probematches-message.md) [ou ResolveMatches.](resolvematches-message.md) A URL usada para troca de metadados aparece na saída do Cliente de Depuração do WSD, prefixada pela frase `Using xAddr` . O exemplo a seguir mostra os XAddrs usados para troca de metadados na saída do cliente de depuração do WSD acima.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Se os XAddrs fornecidos não estão em conformidade com as regras de validação [XAddr,](xaddr-validation-rules.md)o Cliente de Depuração do WSD não poderá obter os metadados do dispositivo.

-   O aplicativo está em execução no contexto de segurança errado. Verifique se o aplicativo está usando as credenciais corretas e se o cliente e o host têm permissão suficiente para acessar a rede.
-   A configuração do firewall está errada. Siga as [](inspecting-adapter-and-firewall-settings.md) instruções em Inspecionando o adaptador e Configurações firewall para verificar se as configurações Windows Firewall do Windows estão corretas e se não há outras regras descartando os pacotes. O cliente e o host também podem ser copiados em um computador "pristine" (um com uma instalação de sistema operacional padrão que nunca foi ingressada em um domínio) para tentar reproduzir a falha.
-   Uma política de IPSec está bloqueando o aplicativo. Copie o cliente e o host em um computador que não está sujeito a políticas de IPSec e tente reproduzir a falha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



