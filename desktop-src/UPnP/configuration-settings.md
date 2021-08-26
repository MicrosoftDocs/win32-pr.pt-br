---
title: Definições de configuração
description: O comportamento da API do ponto de controle e da API de host do dispositivo pode ser modificado alterando as configurações no registro.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68438f6eb425da253aa7f59af3b7d060bacacadb865d4546ddbc0f37fecd9ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008106"
---
# <a name="configuration-settings"></a>Definições de configuração

O comportamento da [API do ponto de controle](control-point-api.md) e da API de host do [dispositivo](device-host-api.md) pode ser modificado alterando as configurações no registro.

Há sete valores de registro que afetam o comportamento:

-   **DownloadScope**
-   **DeviceLifeTime**
-   \\Host de dispositivo **UPnP** \\ **Limite de tamanho de arquivo**
-   \\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de tamanho de arquivo**
-   **MaxCache**
-   **TTL**
-   **ReceiveScope**

Há dois valores de registro chamados **limite de tamanho de arquivo**, um para documentos de descrição e o outro para respostas que usam SOAP (Simple Object Access Protocol).

O local de cada um dos sete valores no registro é o seguinte:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a>Descrições de valor do registro

Os valores do registro são explicados na lista a seguir. Cada valor de registro é um **reg \_ DWORD** (um número inteiro de 32 bits). O efeito de cada valor é global.

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**
</dt> <dd>

Especifica quais endereços IP são válidos para a URL do documento de descrição do dispositivo. Se o endereço IP do host especificado na URL do documento de descrição não estiver dentro do escopo especificado por **DownloadScope**, esse endereço IP não será válido e o objeto do dispositivo não será criado.

Os valores válidos são mostrados na tabela a seguir. O valor padrão é 1.



| Valor de **DownloadScope** | Significado                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | O endereço IP do host deve ser um endereço de sub-rede.                                                                                                                                                                |
| 1                          | O endereço IP do host deve ser um endereço de sub-rede ou um endereço privado que seja um de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (conforme especificado pela RFC 1918) ou 169,254. *x*. *x* (conforme especificado pela RFC 3330). |
| 2                          | O endereço IP do host deve ser um endereço de sub-rede, um endereço privado ou um endereço que esteja dentro dos saltos de tempo de vida (TTL) do ponto de controle.                                                              |
| 3                          | O endereço IP do host pode ser qualquer endereço.                                                                                                                                                                      |
| >3                      | O mesmo que para o valor 0.                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**
</dt> <dd>

Opcional. Especifica o tempo de vida de um dispositivo, em segundos, que substitui o valor fornecido na mensagem de anúncio do dispositivo. Se **DeviceLifeTime** estiver presente, o valor especificado no anúncio do dispositivo será ignorado e o valor do registro será usado em seu lugar. Isso se aplica a todos os dispositivos.

Os valores válidos variam de 900 a **Max \_ DWORD**. O valor padrão é 1800. Se **DeviceLifeTime** for definido como 0, o valor padrão será usado.

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\Host de dispositivo **UPnP** \\ **Limite de tamanho de arquivo**
</dt> <dd>

Especifica o tamanho máximo, em bytes, de cada documento de descrição. essa configuração não é configurável em versões do Windows anteriores Windows XP Service Pack 2. Nas versões anteriores, essa configuração é embutida em código como 102400.

Os valores válidos variam de 10240 a **Max \_ DWORD**. O valor padrão é 102400.

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de tamanho de arquivo**
</dt> <dd>

Especifica o tamanho máximo, em bytes, da resposta SOAP aceitável. essa configuração não é configurável em versões do Windows anteriores Windows XP Service Pack 2. Nas versões anteriores, essa configuração é embutida em código como 102400.

Os valores válidos variam de 10240 a **Max \_ DWORD**. O valor padrão é 102400.

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**
</dt> <dd>

Especifica o número máximo de entradas permitidas no cache SSDP (Simple Service Discovery Protocol).

Os valores válidos variam de 10 a 30000. O valor padrão é 1000.

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**IGUAL**
</dt> <dd>

Especifica a vida útil para um pacote SSDP. Ou seja, **TTL** especifica o número de saltos permitidos para um pacote.

Os valores válidos variam de 1 a 255. O valor padrão é 1.

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**
</dt> <dd>

Especifica quais endereços IP são fontes válidas de uma mensagem. Se uma mensagem de entrada se originar de um endereço que não está dentro do escopo especificado por **ReceiveScope**, a mensagem será ignorada. essa configuração não é configurável em versões do Windows anteriores Windows XP Service Pack 2. Nas versões anteriores, uma mensagem é aceita sem considerar sua origem.

Os valores válidos são mostrados na tabela a seguir. O valor padrão é 1.



| Valor de **ReceiveScope** | Significado                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | O endereço IP do remetente deve ser um endereço de sub-rede.                                                                                                                                                                |
| 1                         | O endereço IP do remetente deve ser um endereço de sub-rede ou um endereço privado que seja um de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (conforme especificado pela RFC 1918) ou 169,254. *x*. *x* (conforme especificado pela RFC 3330). |
| 2                         | Não usado. Se **ReceiveScope** for definido como 2, o valor padrão será usado.                                                                                                                                        |
| 3                         | O endereço IP do remetente pode ser qualquer endereço.                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da arquitetura UPnP](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




