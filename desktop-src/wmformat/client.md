---
title: Log do cliente (Windows Media Format SDK 11)
description: Saiba mais sobre o registro em log do Windows Media Format 11 SDK. O registro em log fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, registro em log do cliente
- Windows Media Format SDK, registro em log
- ASF (Advanced Systems Format), registro em log do cliente
- ASF (Formato de Sistemas Avançados), registro em log do cliente
- FORMATO DE SISTEMAS Avançados (ASF), registro em log
- ASF (Formato de Sistemas Avançados), registro em log
- registro em log do cliente
- registrando clientes em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095e01fcf0730fdec8d06a931a9a988ca79ea77f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406259"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>Log do cliente (Windows Media Format SDK 11)

Quando o objeto leitor lê dados de um servidor, ele envia informações de log para o servidor. Os provedores de conteúdo normalmente usam essas informações para medir a qualidade do serviço, gerar informações de cobrança ou acompanhar a publicidade. As informações de log não contêm dados pessoais.

O aplicativo pode especificar algumas das informações registradas, chamando o método [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) no objeto de leitor. Por exemplo, você pode especificar a cadeia de caracteres user-agent, o nome do aplicativo player ou a página da Web que hospeda o player.

As informações de log incluem um GUID que identifica a sessão. Por padrão, o leitor gera uma ID de sessão anônima. Opcionalmente, o leitor pode enviar uma ID que identifica exclusivamente o usuário atual. Para habilitar esse recurso, chame o método [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) com o **valor TRUE.**

Você pode configurar o objeto de leitor para enviar as informações de log para outro servidor, além do servidor de origem. Para fazer isso, chame o método [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) com a URL do servidor. Essa URL deve apontar para um script ou executável que possa lidar com solicitações HTTP GET e POST. Você pode usar o Agente de Anúncio multicast e log (wmsiislog.dll) ou pode escrever um script ASP ou CGI personalizado para receber os dados de log.

> [!Note]  
> Você pode obter a mesma funcionalidade criando uma playlist do lado do servidor com um **atributo logURL.**

 

Quando o objeto de leitor envia o log, ele faz o seguinte:

1.  Envia uma solicitação GET vazia para o servidor.
2.  Analisar a resposta do servidor para uma das seguintes cadeias de caracteres:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` em que "0.0.0.0" é qualquer número de versão válido.
3.  Envia uma solicitação POST com as informações de log.

O código a seguir mostra um script ASP de exemplo que recebe as informações de registro em log e as grava em um arquivo:


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



Você pode especificar vários servidores para receber informações de log; basta chamar **AddLoggingUrl** uma vez com cada URL. Para limpar a lista de servidores que recebem logs, chame o [**método IWMReaderNetworkConfig::ResetLoggingUrlList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> <dt>

[**IWMReaderAdvanced Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**IWMReaderAdvanced2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




