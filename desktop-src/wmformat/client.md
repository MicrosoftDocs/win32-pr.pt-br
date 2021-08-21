---
title: log do cliente (Windows Media Format 11 SDK)
description: saiba mais sobre o log do cliente para Windows SDK do formato de mídia 11. O registro em log fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows SDK de formato de mídia, log de cliente
- Windows SDK do formato de mídia, registrando
- ASF (Advanced Systems Format), log de cliente
- ASF (formato de sistemas avançados), log de cliente
- ASF (Advanced Systems Format), registro em log
- ASF (formato de sistemas avançados), registro em log
- log de cliente
- registrando clientes em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460058d6ad4009fab301c6ce322df3144bdd0e5d9bb4732d54126f7675cd9e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028024"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>log do cliente (Windows Media Format 11 SDK)

Quando o objeto leitor lê dados de um servidor, ele envia informações de log para o servidor. Os provedores de conteúdo normalmente usam essas informações para medir a qualidade do serviço, gerar informações de cobrança ou acompanhar anúncios. As informações de registro em log não contêm dados pessoais.

O aplicativo pode especificar algumas das informações que são registradas, chamando o método [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) no objeto Reader. Por exemplo, você pode especificar a cadeia de caracteres do agente do usuário, o nome do aplicativo de Player ou a página da Web que hospeda o Player.

As informações de log incluem um GUID que identifica a sessão. Por padrão, o leitor gera uma ID de sessão anônima. Opcionalmente, o leitor pode, em vez disso, enviar uma ID que identifica exclusivamente o usuário atual. Para habilitar esse recurso, chame o método [**IWMReaderAdvanced2:: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) com o valor **true**.

Você pode configurar o objeto leitor para enviar as informações de log para outro servidor, além do servidor de origem. Para fazer isso, chame o método [**IWMReaderNetworkConfig:: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) com a URL do servidor. Essa URL deve apontar para um script ou executável que pode manipular solicitações HTTP GET e POST. Você pode usar o agente de anúncio de log e multicast (wmsiislog.dll) ou pode gravar um script ASP ou CGI personalizado para receber os dados de log.

> [!Note]  
> Você pode obter a mesma funcionalidade criando uma lista de reprodução no lado do servidor com um atributo **LogURL** .

 

Quando o objeto do leitor envia o log, ele faz o seguinte:

1.  Envia uma solicitação GET vazia para o servidor.
2.  Analisa a resposta do servidor para uma das seguintes cadeias de caracteres:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` onde "0.0.0.0" é qualquer número de versão válido.
3.  Envia uma solicitação POST com as informações de log.

O código a seguir mostra um exemplo de script ASP que recebe as informações de registro em log e grava-as em um arquivo:


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



Você pode especificar vários servidores para receber informações de registro em log; Basta chamar **AddLoggingUrl** uma vez com cada URL. Para limpar a lista de servidores que recebem logs, chame o método [**IWMReaderNetworkConfig:: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> <dt>

[**Interface IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




