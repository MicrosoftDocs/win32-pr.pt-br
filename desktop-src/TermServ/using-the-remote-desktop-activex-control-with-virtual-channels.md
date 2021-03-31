---
title: Usando o controle ActiveX Área de Trabalho Remota com canais virtuais
description: Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para os computadores cliente.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822704"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Usando o controle ActiveX Área de Trabalho Remota com canais virtuais

Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para os computadores cliente que acessam o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio do controle ActiveX Área de Trabalho Remota.

**Para disponibilizar um aplicativo de canal virtual**

1.  Implante o módulo do lado do servidor do aplicativo e verifique se ele está em execução no servidor de Host da Sessão RD. Na página conexão do aplicativo Web Serviços de Área de Trabalho Remota em execução no servidor Web, acesse a propriedade **PluginDlls** da interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) para especificar o nome da sua DLL de canal virtual. Se você tiver mais de um plug-in, especifique uma lista delimitada por vírgulas de nomes de DLL. Por exemplo, se o seu plug-in de canal virtual for nomeado "MyPlugin.dll", use o seguinte código:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Use o código a seguir se você tiver duas DLLs de canal virtual. Neste exemplo, os nomes de arquivo DLL são "MyPlugin.dll" e "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Por motivos de segurança, a propriedade **PluginDlls** aceita apenas uma lista nomeada de DLLs de canal virtual. O controle retornará um erro se qualquer forma de sistema de arquivos ou caminho UNC for especificada. Além disso, os nomes das DLLs devem conter apenas caracteres alfanuméricos.

2.  Verifique se o módulo do lado do cliente está instalado no diretório% windir% \\ System32.

A API de canal virtual não permite que várias instâncias da mesma DLL de canal virtual sejam carregadas em um único processo. Por isso, se houver várias instâncias do Área de Trabalho Remota controle ActiveX em execução dentro do mesmo processo, somente a primeira instância do controle poderá carregar a DLL do canal virtual. Se você estiver criando um aplicativo de canal virtual que deve dar suporte a várias instâncias em um único processo, deverá usar a API de [canais virtuais dinâmicos](dynamic-virtual-channels.md) para implementar seu aplicativo de canal virtual.

> [!Note]  
> Por padrão, o controle ActiveX Área de Trabalho Remota carrega as DLLs de cliente do canal virtual do diretório% windir% \\ System32. É possível que um administrador altere esse diretório de DLL de plug-in de cliente padrão. Para fazer isso, edite a chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** no computador cliente. Este caminho de diretório não pode ser especificado no formato UNC.

 

 

 




