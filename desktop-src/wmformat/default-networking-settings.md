---
title: Rede padrão Configurações
description: Rede padrão Configurações
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows SDK de Formato de Mídia, configurações de rede padrão
- ASF (Advanced Systems Format), configurações de rede padrão
- ASF (Formato de Sistemas Avançados), configurações de rede padrão
- Windows SDK de Formato de Mídia, configurações de rede
- ASF (Advanced Systems Format), configurações de rede
- ASF (Formato de Sistemas Avançados), configurações de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591bf4aa2154d5cc04a8a17b5fc75f290a8493a39d530d4246bc0338c2424e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931416"
---
# <a name="default-networking-settings"></a>Rede padrão Configurações

As tabelas a seguir descrevem as configurações padrão dos parâmetros de rede no SDK Windows Formato de Mídia, agrupados por interface.



| IWMReaderNetworkConfig                | Configuração padrão              |
|---------------------------------------|------------------------------|
| Tempo de buffer                        | 5 segundos                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (não válido)                |
| ProxySetting: HTTP                    | NAVEGADOR DE CONFIGURAÇÃO \_ DE PROXY \_ WMT \_ |
| ProxySetting: MMS                     | CONFIGURAÇÃO DE PROXY WMT \_ \_ \_ NONE    |
| ProxySetting: RTSP                    | CONFIGURAÇÃO DE PROXY WMT \_ \_ \_ NONE    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort: HTTP                       | 80                           |
| ProxyPort: MMS                        | 1755                         |
| ProxtPort: RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | FALSE                        |
| ForceRerunAutoDetection               | FALSE                        |
| EnableMulticast                       | TRUE                         |
| EnableHTTP                            | TRUE                         |
| EnableTCP                             | TRUE                         |
| EnableUDP                             | TRUE                         |
| Largura de banda da conexão                  | 0 (detecção automática)              |



 



| IWMReaderNetworkConfig2        | Configuração padrão        |
|--------------------------------|------------------------|
| Duração acelerada do streaming | 100000000 (10 segundos) |
| Habilitar o cache de conteúdo         | TRUE                   |
| Habilitar cache rápido              | TRUE                   |
| Habilitar reends                 | TRUE                   |
| Habilitar a afinação de conteúdo        | TRUE                   |
| Limite de reconexão                | 25                     |



 



| IWMWriterNetworkSink | Configuração padrão         |
|----------------------|-------------------------|
| Máximo de clientes      | 5                       |
| Protocolo de rede     | 0 (PROTOCOLO WMT \_ \_ HTTP) |
| Host URL             | 0 (não válido)           |



 



| IWMWriterAdvanced2  | Configuração padrão             |
|---------------------|-----------------------------|
| Tamanho máximo do pacote | 1.400                        |
| ID do cliente de log       | FALSE                       |
| Modo de reprodução           | SELEÇÃO AUTOMÁTICA DO MODO DE REPRODUÇÃO \_ \_ DO \_ WMT |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> </dl>

 

 




