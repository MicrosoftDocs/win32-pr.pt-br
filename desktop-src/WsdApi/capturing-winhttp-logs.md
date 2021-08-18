---
description: Os logs de WinHTTP podem ser usados para ajudar a solucionar problemas de aplicativos WSDAPI. Isso é útil quando a troca de metadados falha ou quando a negociação SSL/TLS falha.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Capturando logs do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 648ebb95182096fc4a853c2685f896fa2902a828c8ed0ab143ce89c04831c7ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991776"
---
# <a name="capturing-winhttp-logs"></a>Capturando logs do WinHTTP

Os logs de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) podem ser usados para ajudar a solucionar problemas de aplicativos WSDAPI. Isso é útil quando a troca de metadados falha ou quando a negociação SSL/TLS falha.

Este procedimento mostra como capturar logs do WinHTTP no PC cliente. O aplicativo cliente baseado em WSDAPI não deve estar em execução quando o log está habilitado. Se o aplicativo cliente estiver em execução quando o log estiver habilitado, o cliente e/ou o PC deverão ser reiniciados antes de WS-Discovery e o tráfego de troca de metadados aparecerá nos logs do WinHTTP.

**Para capturar logs do WinHTTP**

1.  Abra uma janela de prompt de comandos com privilégios elevados no computador cliente.
2.  Execute o seguinte comando: **netsh WinHTTP set tracing Trace-File-prefixo = "C: \\ temp \\ DPWS" level = verbose Format = estado ANSI = Enabled Max-Trace-File-Size = 1073741824**

    Esse comando habilita o log do WinHTTP. Todos os arquivos de log serão armazenados no diretório C: \\ temp e os nomes de arquivo começarão com o prefixo DPWS. No máximo 1 GB de arquivos de log serão armazenados.

3.  Se o processo que usa o WinHTTP no cliente já estiver em execução, reinicie o computador. Por exemplo, se as APIs de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) estiverem sendo usadas, o computador deverá ser reiniciado. As APIs de descoberta de função chamam WinHTTP de dentro de um host de serviço, que pode já ter começado quando o rastreamento foi habilitado.
4.  Inicie o aplicativo cliente baseado em WSDAPI. O aplicativo que está sendo depurado ou o cliente de depuração WSD pode ser usado.
5.  Reproduzir a falha do aplicativo.
6.  Encerrar o aplicativo cliente baseado em WSDAPI.
7.  Se o processo que usa o WinHTTP não for encerrado com o aplicativo cliente, reinicie o computador. Por exemplo, se as APIs de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) estiverem sendo usadas, o computador deverá ser reiniciado.
8.  Execute o seguinte comando: **netsh WinHTTP definir estado de rastreamento = desabilitado**

    Este comando desabilita o log do WinHTTP.

9.  Inspecione os logs do DPWS em C: \\ temp e verifique se as solicitações e mensagens necessárias foram enviadas.
10. Se a comunicação de canal seguro (HTTPS) estiver sendo usada, verifique se há falhas de SSL/TLS.

Depois que os logs do WinHTTP tiverem sido capturados, os logs poderão ser examinados para procurar a causa de uma falha do aplicativo WSDAPI. Observe que o editor de texto usado para exibir esses logs deve ser executado como administrador. Para obter mais informações, consulte [usando o log do WinHTTP para verificar se há tráfego](using-winhttp-logging-to-verify-get-traffic.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Usando o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
