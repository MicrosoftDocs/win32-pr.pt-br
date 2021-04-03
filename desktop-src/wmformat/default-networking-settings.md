---
title: Configurações de rede padrão
description: Configurações de rede padrão
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- SDK do Windows Media Format, configurações de rede padrão
- Formato de sistema avançado (ASF), configurações de rede padrão
- ASF (formato de sistemas avançados), configurações de rede padrão
- SDK do Windows Media Format, configurações de rede
- ASF (Advanced Systems Format), configurações de rede
- ASF (formato de sistemas avançados), configurações de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823022"
---
# <a name="default-networking-settings"></a>Configurações de rede padrão

As tabelas a seguir descrevem as configurações padrão dos parâmetros de rede no Windows Media Format SDK, agrupadas por interface.



| IWMReaderNetworkConfig                | Configuração padrão              |
|---------------------------------------|------------------------------|
| Tempo de buffer                        | 5 segundos                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (não é válido)                |
| ProxySetting: HTTP                    | \_navegador de \_ configurações de proxy WMT \_ |
| ProxySetting: MMS                     | \_configuração de proxy WMT \_ \_ None    |
| ProxySetting: RTSP                    | \_configuração de proxy WMT \_ \_ None    |
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
| Duração de streaming acelerada | 100 milhões (10 segundos) |
| Habilitar o Caching de conteúdo         | TRUE                   |
| Habilitar cache rápido              | TRUE                   |
| Habilitar reenvios                 | TRUE                   |
| Habilitar o estreitamento de conteúdo        | TRUE                   |
| Limite de reconexão                | 25                     |



 



| IWMWriterNetworkSink | Configuração padrão         |
|----------------------|-------------------------|
| Máximo de clientes      | 5                       |
| Protocolo de rede     | 0 ( \_ protocolo \_ http WMT) |
| URL do host             | 0 (não é válido)           |



 



| IWMWriterAdvanced2  | Configuração padrão             |
|---------------------|-----------------------------|
| Tamanho máximo do pacote | 1.400                        |
| ID do cliente de log       | FALSE                       |
| Modo de reprodução           | SELEÇÃO asWMT de \_ modo de reprodução \_ \_ |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> </dl>

 

 




