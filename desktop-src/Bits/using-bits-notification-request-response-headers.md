---
title: Usando cabeçalhos de solicitação/resposta de notificação do BITS
description: O BITS pode enviar o local do arquivo de carregamento (por referência) para seu aplicativo de servidor ou pode enviar o arquivo de upload no corpo da solicitação (por valor).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159351"
---
# <a name="using-bits-notification-requestresponse-headers"></a><span data-ttu-id="87e4d-103">Usando cabeçalhos de solicitação/resposta de notificação do BITS</span><span class="sxs-lookup"><span data-stu-id="87e4d-103">Using BITS Notification Request/Response Headers</span></span>

<span data-ttu-id="87e4d-104">O BITS pode enviar o local do arquivo de carregamento (por referência) para seu aplicativo de servidor ou pode enviar o arquivo de upload no corpo da solicitação (por valor).</span><span class="sxs-lookup"><span data-stu-id="87e4d-104">BITS can send the location of the upload file (by reference) to your server application or it can send the upload file in the body of the request (by value).</span></span> <span data-ttu-id="87e4d-105">Para especificar como o BITS envia o arquivo de upload para o aplicativo de servidor, defina a propriedade metabase do IIS, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="87e4d-105">To specify how BITS sends the upload file to your server application, set the IIS metabase property, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="87e4d-106">Se você especificar por referência, o BITS passará o local do arquivo no cabeçalho BITS-Request-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="87e4d-106">If you specify by reference, BITS passes the location of the file in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="87e4d-107">Para enviar uma resposta, crie e grave sua resposta para o arquivo especificado no cabeçalho BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="87e4d-107">To send a reply, create and write your response to the file specified in the BITS-Response-DataFile-Name header.</span></span>

<span data-ttu-id="87e4d-108">Os aplicativos de servidor que enviam a mesma resposta a muitos clientes devem usar por referência, portanto, há apenas uma cópia da resposta no servidor.</span><span class="sxs-lookup"><span data-stu-id="87e4d-108">Server applications that send the same reply to many clients should use by reference, so there is only one copy of the reply on the server.</span></span> <span data-ttu-id="87e4d-109">Por exemplo, em um aplicativo de atualização de software, o cliente carregaria sua configuração de software no aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="87e4d-109">For example, in a software update application, the client would upload its software configuration to the server application.</span></span> <span data-ttu-id="87e4d-110">O aplicativo de servidor determina qual pacote o cliente precisa e envia a URL do pacote para o BITS.</span><span class="sxs-lookup"><span data-stu-id="87e4d-110">The server application determines which package the client needs and sends the URL of the package to BITS.</span></span> <span data-ttu-id="87e4d-111">Em seguida, o BITS baixa o pacote como a resposta.</span><span class="sxs-lookup"><span data-stu-id="87e4d-111">Then, BITS downloads the package as the reply.</span></span>

<span data-ttu-id="87e4d-112">Os aplicativos de servidor que geram respostas exclusivas para cada cliente devem usar por valor.</span><span class="sxs-lookup"><span data-stu-id="87e4d-112">Server applications that generate unique replies for each client should use by value.</span></span> <span data-ttu-id="87e4d-113">Por exemplo, um aplicativo de servidor que dá suporte à compra de arquivos de música precisaria enviar um arquivo de música assinado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="87e4d-113">For example, a server application that supports the purchase of music files would need to send a signed music file to the client.</span></span> <span data-ttu-id="87e4d-114">Como o arquivo de música assinado é exclusivo para o cliente, o aplicativo de servidor não o armazena no servidor.</span><span class="sxs-lookup"><span data-stu-id="87e4d-114">Because the signed music file is unique to the client, the server application would not store it on the server.</span></span> <span data-ttu-id="87e4d-115">Por valor também é útil para um aplicativo que já está escrito para aceitar dados do cliente Web diretamente.</span><span class="sxs-lookup"><span data-stu-id="87e4d-115">By value is also useful for an application that is already written to accept web client data directly.</span></span>

<span data-ttu-id="87e4d-116">Para obter detalhes sobre os cabeçalhos de solicitação e resposta usados entre o BITS e o aplicativo de servidor, consulte [protocolo de notificação para aplicativos de servidor](notification-protocol-for-server-applications.md).</span><span class="sxs-lookup"><span data-stu-id="87e4d-116">For details on the request and response headers used between BITS and your server application, see [Notification Protocol for Server Applications](notification-protocol-for-server-applications.md).</span></span>

<span data-ttu-id="87e4d-117">O exemplo de JavaScript a seguir mostra como acessar os arquivos de solicitação e resposta em um aplicativo de servidor que usa por notificação de referência (o BITS passa o local dos arquivos nos cabeçalhos).</span><span class="sxs-lookup"><span data-stu-id="87e4d-117">The following JavaScript example shows how to access the request and response files in a server application that uses by reference notification (BITS passes the location of the files in the headers).</span></span>


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



<span data-ttu-id="87e4d-118">Se você quiser usar um arquivo de resposta diferente daquele especificado em BITS-Response-DataFile-Name, chame o método **Response. AddHeader** para adicionar o bits-static-Response-URL, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="87e4d-118">If you want to use a different response file than the one specified in BITS-Response-DataFile-Name, call the **Response.AddHeader** method to add the BITS-Static-Response-URL as shown in the following example.</span></span> <span data-ttu-id="87e4d-119">Se você especificar um arquivo de resposta diferente, não crie o arquivo de resposta especificado em BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="87e4d-119">If you specify a different response file, do not create the response file specified in BITS-Response-DataFile-Name.</span></span>


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




