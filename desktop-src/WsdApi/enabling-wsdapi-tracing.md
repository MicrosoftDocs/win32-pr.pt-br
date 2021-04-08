---
description: Os logs de WSDAPI contêm informações de depuração que podem ser usadas para encontrar a causa raiz das falhas do aplicativo WSDAPI.
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: Habilitando o rastreamento WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951f8ddfee6043cc662a456c70960e78ed1a3625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010812"
---
# <a name="enabling-wsdapi-tracing"></a>Habilitando o rastreamento WSDAPI

Os logs de WSDAPI contêm informações de depuração que podem ser usadas para encontrar a causa raiz das falhas do aplicativo WSDAPI. Quando o rastreamento está habilitado, as informações de log são armazenadas em um arquivo. etl em um local especificado pelo usuário. Esse arquivo. etl pode ser enviado para o suporte do desenvolvedor da Microsoft para análise da causa raiz. Para obter informações sobre como contatar o suporte, acesse [https://support.microsoft.com](https://support.microsoft.com) .

Esse procedimento deve ser feito duas vezes: uma vez no cliente e uma vez no host.

**Para habilitar o rastreamento WSDAPI**

1.  Usando o bloco de notas ou outro editor de texto, crie um arquivo de texto com o seguinte texto:

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  Salve o arquivo de texto como `C:\temp\traceguids.txt` e feche o arquivo.
3.  Abra uma janela de prompt de comando elevado.
4.  Execute o seguinte comando: **logman.exe Create Trace wsdlog-o c: \\ temp \\ WSD**
5.  Execute o seguinte comando: **logman.exe Update wsdlog-PF c: \\ temp \\traceguids.txt**
6.  Execute o seguinte comando: **logman.exe Start wsdlog**
7.  Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de rede.

**Para desabilitar o rastreamento WSDAPI**

1.  Abra uma janela de prompt de comando elevado.
2.  Execute o seguinte comando: **logman.exe parar wsdlog**

Depois que a falha do aplicativo for capturada, os \* arquivos. etl poderão ser enviados ao suporte da Microsoft. Esses arquivos estão localizados em `C:\temp\wsd_*.etl` .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



