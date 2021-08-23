---
title: Usando cabeçalhos de solicitação/resposta de notificação do BITS
description: O BITS pode enviar o local do arquivo de carregamento (por referência) para seu aplicativo de servidor ou pode enviar o arquivo de upload no corpo da solicitação (por valor).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3db568f483468cbc92474f24f830da5bf1be94a2165cbb69a2d1751cc58965dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021064"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Usando cabeçalhos de solicitação/resposta de notificação do BITS

O BITS pode enviar o local do arquivo de carregamento (por referência) para seu aplicativo de servidor ou pode enviar o arquivo de upload no corpo da solicitação (por valor). Para especificar como o BITS envia o arquivo de upload para o aplicativo de servidor, defina a propriedade metabase do IIS, [**BITSServerNotificationType**](bits-iis-extension-properties.md). Se você especificar por referência, o BITS passará o local do arquivo no cabeçalho BITS-Request-DataFile-Name. Para enviar uma resposta, crie e grave sua resposta para o arquivo especificado no cabeçalho BITS-Response-DataFile-Name.

Os aplicativos de servidor que enviam a mesma resposta a muitos clientes devem usar por referência, portanto, há apenas uma cópia da resposta no servidor. Por exemplo, em um aplicativo de atualização de software, o cliente carregaria sua configuração de software no aplicativo de servidor. O aplicativo de servidor determina qual pacote o cliente precisa e envia a URL do pacote para o BITS. Em seguida, o BITS baixa o pacote como a resposta.

Os aplicativos de servidor que geram respostas exclusivas para cada cliente devem usar por valor. Por exemplo, um aplicativo de servidor que dá suporte à compra de arquivos de música precisaria enviar um arquivo de música assinado ao cliente. Como o arquivo de música assinado é exclusivo para o cliente, o aplicativo de servidor não o armazena no servidor. Por valor também é útil para um aplicativo que já está escrito para aceitar dados do cliente Web diretamente.

Para obter detalhes sobre os cabeçalhos de solicitação e resposta usados entre o BITS e o aplicativo de servidor, consulte [protocolo de notificação para aplicativos de servidor](notification-protocol-for-server-applications.md).

O exemplo de JavaScript a seguir mostra como acessar os arquivos de solicitação e resposta em um aplicativo de servidor que usa por notificação de referência (o BITS passa o local dos arquivos nos cabeçalhos).


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



Se você quiser usar um arquivo de resposta diferente daquele especificado em BITS-Response-DataFile-Name, chame o método **Response. AddHeader** para adicionar o bits-static-Response-URL, conforme mostrado no exemplo a seguir. Se você especificar um arquivo de resposta diferente, não crie o arquivo de resposta especificado em BITS-Response-DataFile-Name.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




