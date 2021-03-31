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
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Gravando um script para configurar o diretório virtual

Você pode usar os valores padrão da propriedade IIS do BITS para carregar um arquivo no servidor. O arquivo de carregamento é gravado na URL, conforme especificado no nome do arquivo remoto do trabalho. Para carregar o arquivo em um aplicativo de servidor e receber uma resposta, altere a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) para enviar os dados por referência (envia o nome do arquivo que contém os dados) ou por valor (envia os dados no corpo da solicitação).

Para obter uma lista e uma descrição das propriedades que você pode modificar, consulte [Propriedades de extensão do IIS do bits](bits-iis-extension-properties.md). Use os métodos da interface [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) para habilitar e desabilitar o diretório virtual para carregamentos.

O exemplo a seguir mostra como usar o Windows Script Host para criar, configurar e habilitar um diretório virtual do IIS para carregamentos do BITS.


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



Para alterar o exemplo anterior para carregar os dados em um aplicativo de servidor, adicione o código a seguir antes de **setinfo**.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



O local do arquivo de carregamento é passado para o aplicativo de servidor, myasp. asp, no cabeçalho BITS-Request-DataFile-Name. Para receber o arquivo de upload no corpo da solicitação, defina a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) como 2.

Para obter informações sobre como receber os dados de upload em seu aplicativo de servidor, consulte [usando cabeçalhos de solicitação/resposta de notificação do bits](using-bits-notification-request-response-headers.md).

 

 




