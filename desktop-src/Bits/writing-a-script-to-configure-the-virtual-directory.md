---
title: Gravando um script para configurar o diretório virtual
description: Gravando um script para configurar o diretório virtual
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915969"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="95f01-103">Gravando um script para configurar o diretório virtual</span><span class="sxs-lookup"><span data-stu-id="95f01-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="95f01-104">Você pode usar os valores padrão da propriedade IIS do BITS para carregar um arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="95f01-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="95f01-105">O arquivo de carregamento é gravado na URL, conforme especificado no nome do arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="95f01-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="95f01-106">Para carregar o arquivo em um aplicativo de servidor e receber uma resposta, altere a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) para enviar os dados por referência (envia o nome do arquivo que contém os dados) ou por valor (envia os dados no corpo da solicitação).</span><span class="sxs-lookup"><span data-stu-id="95f01-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="95f01-107">Para obter uma lista e uma descrição das propriedades que você pode modificar, consulte [Propriedades de extensão do IIS do bits](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="95f01-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="95f01-108">Use os métodos da interface [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) para habilitar e desabilitar o diretório virtual para carregamentos.</span><span class="sxs-lookup"><span data-stu-id="95f01-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="95f01-109">O exemplo a seguir mostra como usar o Windows Script Host para criar, configurar e habilitar um diretório virtual do IIS para carregamentos do BITS.</span><span class="sxs-lookup"><span data-stu-id="95f01-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



<span data-ttu-id="95f01-110">Para alterar o exemplo anterior para carregar os dados em um aplicativo de servidor, adicione o código a seguir antes de **setinfo**.</span><span class="sxs-lookup"><span data-stu-id="95f01-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="95f01-111">O local do arquivo de carregamento é passado para o aplicativo de servidor, myasp. asp, no cabeçalho BITS-Request-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="95f01-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="95f01-112">Para receber o arquivo de upload no corpo da solicitação, defina a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) como 2.</span><span class="sxs-lookup"><span data-stu-id="95f01-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="95f01-113">Para obter informações sobre como receber os dados de upload em seu aplicativo de servidor, consulte [usando cabeçalhos de solicitação/resposta de notificação do bits](using-bits-notification-request-response-headers.md).</span><span class="sxs-lookup"><span data-stu-id="95f01-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




