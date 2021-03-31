---
title: Protocolo de notificação para aplicativos de servidor
description: O BITS usa a propriedade BITSServerNotificationType para determinar como o BITS envia o conteúdo do arquivo de carregamento para o aplicativo de servidor.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916015"
---
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="9fad7-103">Protocolo de notificação para aplicativos de servidor</span><span class="sxs-lookup"><span data-stu-id="9fad7-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="9fad7-104">O BITS usa a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) para determinar como o bits envia o conteúdo do arquivo de carregamento para o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="9fad7-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="9fad7-105">Se a propriedade BITSServerNotificationType for definida como 1, [o bits passará o local do arquivo de carregamento em um cabeçalho](#sending-the-location-of-the-upload-file-in-a-header).</span><span class="sxs-lookup"><span data-stu-id="9fad7-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="9fad7-106">Se a propriedade BITSServerNotificationType for definida como 2, [o bits passará o conteúdo do arquivo de carregamento no corpo da solicitação](#sending-the-upload-file-in-the-body-of-the-request).</span><span class="sxs-lookup"><span data-stu-id="9fad7-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="9fad7-107">Para obter detalhes sobre como o BITS lida com erros do aplicativo de servidor, consulte [Manipulando erros de aplicativo do servidor](#handling-server-application-errors).</span><span class="sxs-lookup"><span data-stu-id="9fad7-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="9fad7-108">Enviando o local do arquivo de carregamento em um cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9fad7-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="9fad7-109">O BITS passará o local dos arquivos de upload e de resposta para o aplicativo de servidor nos cabeçalhos, se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) estiver definida como 1.</span><span class="sxs-lookup"><span data-stu-id="9fad7-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="9fad7-110">O aplicativo de servidor abre o arquivo de upload, processa os dados e, em seguida, gera o arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="9fad7-111">Por padrão, o BITS remove os arquivos de upload e de resposta do servidor depois de receber a resposta do aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="9fad7-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="9fad7-112">Para que o BITS Copie o arquivo de upload para o local especificado pelo nome do arquivo remoto no trabalho, inclua o cabeçalho BITS-Copy-file-to-Destination em sua resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="9fad7-113">Se você não incluir o cabeçalho e quiser salvar os arquivos de upload e de resposta, deverá copiar os arquivos de upload e de resposta em um novo local antes de responder.</span><span class="sxs-lookup"><span data-stu-id="9fad7-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="9fad7-114">A tabela a seguir mostra os cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9fad7-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="9fad7-115">Cabeçalho da solicitação</span><span class="sxs-lookup"><span data-stu-id="9fad7-115">Request header</span></span>              | <span data-ttu-id="9fad7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fad7-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fad7-117">BITS-original-solicitação-URL</span><span class="sxs-lookup"><span data-stu-id="9fad7-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="9fad7-118">Contém o nome remoto especificado no trabalho.</span><span class="sxs-lookup"><span data-stu-id="9fad7-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="9fad7-119">BITS-Request-DataFile-Name</span><span class="sxs-lookup"><span data-stu-id="9fad7-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="9fad7-120">Contém o caminho completo para os dados carregados.</span><span class="sxs-lookup"><span data-stu-id="9fad7-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="9fad7-121">BITS-Response-DataFile-Name</span><span class="sxs-lookup"><span data-stu-id="9fad7-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="9fad7-122">Contém o caminho completo para onde o BITS espera que o aplicativo de servidor grave a resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="9fad7-123">A tabela a seguir mostra os cabeçalhos de resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="9fad7-124">Cabeçalho de resposta</span><span class="sxs-lookup"><span data-stu-id="9fad7-124">Response header</span></span>               | <span data-ttu-id="9fad7-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fad7-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fad7-126">BITS-estático-resposta-URL</span><span class="sxs-lookup"><span data-stu-id="9fad7-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="9fad7-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9fad7-127">Optional.</span></span> <span data-ttu-id="9fad7-128">Contém a URL absoluta (não especifique uma URL relativa) para um arquivo de dados estático a ser usado como resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="9fad7-129">O arquivo de dados estáticos deve ser acessível pelo cliente BITS.</span><span class="sxs-lookup"><span data-stu-id="9fad7-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="9fad7-130">Se você usar esse cabeçalho, não crie o arquivo de resposta especificado no cabeçalho de solicitação BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="9fad7-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="9fad7-131">Observe que o BITS não exclui esse arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="9fad7-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="9fad7-132">BITS-Copiar-arquivo-para-destino</span><span class="sxs-lookup"><span data-stu-id="9fad7-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="9fad7-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9fad7-133">Optional.</span></span> <span data-ttu-id="9fad7-134">Por padrão, se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) for definida como 1 ou 2, o servidor bits não copiará o arquivo de carregamento para o local especificado pelo nome do arquivo remoto no trabalho.</span><span class="sxs-lookup"><span data-stu-id="9fad7-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="9fad7-135">Para que o BITS Copie o arquivo para o local especificado pelo nome do arquivo remoto no trabalho, envie este cabeçalho de resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="9fad7-136">Você pode especificar qualquer valor; O BITS não usa o valor.</span><span class="sxs-lookup"><span data-stu-id="9fad7-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="9fad7-137">Observe que as pastas no caminho do arquivo remoto devem existir.</span><span class="sxs-lookup"><span data-stu-id="9fad7-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="9fad7-138">A solicitação a seguir mostra o BITS enviando o local do arquivo de carregamento para o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="9fad7-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

<span data-ttu-id="9fad7-139">O seguinte mostra a resposta do aplicativo do servidor para o BITS; a resposta é colocada no arquivo especificado pelo cabeçalho de solicitação BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="9fad7-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="9fad7-140">Enviando o arquivo de carregamento no corpo da solicitação</span><span class="sxs-lookup"><span data-stu-id="9fad7-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="9fad7-141">O BITS enviará o arquivo de carregamento no corpo da solicitação se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) estiver definida como 2.</span><span class="sxs-lookup"><span data-stu-id="9fad7-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="9fad7-142">O envio do arquivo de upload no corpo da solicitação permite que os scripts e aplicativos existentes funcionem com modificações mínimas.</span><span class="sxs-lookup"><span data-stu-id="9fad7-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="9fad7-143">O arquivo de upload e o arquivo de resposta são passados na solicitação e na resposta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9fad7-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="9fad7-144">A tabela a seguir mostra o cabeçalho da solicitação.</span><span class="sxs-lookup"><span data-stu-id="9fad7-144">The following table shows the request header.</span></span>



| <span data-ttu-id="9fad7-145">Cabeçalho da solicitação</span><span class="sxs-lookup"><span data-stu-id="9fad7-145">Request header</span></span>            | <span data-ttu-id="9fad7-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fad7-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="9fad7-147">BITS-original-solicitação-URL</span><span class="sxs-lookup"><span data-stu-id="9fad7-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="9fad7-148">Contém o nome remoto especificado no trabalho.</span><span class="sxs-lookup"><span data-stu-id="9fad7-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="9fad7-149">A tabela a seguir mostra os cabeçalhos de resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="9fad7-150">Cabeçalho de resposta</span><span class="sxs-lookup"><span data-stu-id="9fad7-150">Response header</span></span>               | <span data-ttu-id="9fad7-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fad7-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fad7-152">BITS-estático-resposta-URL</span><span class="sxs-lookup"><span data-stu-id="9fad7-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="9fad7-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9fad7-153">Optional.</span></span> <span data-ttu-id="9fad7-154">Contém a URL absoluta (não especifique uma URL relativa) para um arquivo de dados estático a ser usado como resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="9fad7-155">O arquivo de dados estáticos deve ser acessível pelo cliente BITS.</span><span class="sxs-lookup"><span data-stu-id="9fad7-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="9fad7-156">Se você usar esse cabeçalho, não inclua a resposta no fluxo.</span><span class="sxs-lookup"><span data-stu-id="9fad7-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="9fad7-157">Observe que o BITS não exclui esse arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="9fad7-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9fad7-158">BITS-Copiar-arquivo-para-destino</span><span class="sxs-lookup"><span data-stu-id="9fad7-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="9fad7-159">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9fad7-159">Optional.</span></span> <span data-ttu-id="9fad7-160">Se a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) for definida como 1 ou 2, o servidor bits não copiará o arquivo de carregamento para o local especificado pelo nome do arquivo remoto no trabalho.</span><span class="sxs-lookup"><span data-stu-id="9fad7-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="9fad7-161">Para que o BITS Copie o arquivo para o local especificado pelo nome do arquivo remoto, envie este cabeçalho de resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="9fad7-162">Você pode especificar qualquer valor; O BITS não usa o valor.</span><span class="sxs-lookup"><span data-stu-id="9fad7-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="9fad7-163">Observe que as pastas no caminho do arquivo remoto devem existir.</span><span class="sxs-lookup"><span data-stu-id="9fad7-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="9fad7-164">A solicitação a seguir mostra o BITS que transmite o arquivo carregado para o aplicativo de servidor no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="9fad7-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="9fad7-165">A resposta a seguir mostra o aplicativo de servidor que passa os dados de resposta para BITS no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="9fad7-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="9fad7-166">Manipulando erros de aplicativo do servidor</span><span class="sxs-lookup"><span data-stu-id="9fad7-166">Handling server application errors</span></span>

<span data-ttu-id="9fad7-167">Consulte [tratamento de erros de aplicativo do servidor](handling-server-application-errors.md).</span><span class="sxs-lookup"><span data-stu-id="9fad7-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





