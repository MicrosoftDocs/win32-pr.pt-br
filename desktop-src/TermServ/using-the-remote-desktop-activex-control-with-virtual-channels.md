---
title: Usando o controle Área de Trabalho Remota ActiveX com canais virtuais
description: Se você habilitar um aplicativo de canais virtuais em sua implantação Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para computadores cliente.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dae33c059a84422788bc49d47f95e0011f78930054ed3884669e8f35763461b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868726"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Usando o controle Área de Trabalho Remota ActiveX com canais virtuais

Se você habilitar um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para computadores cliente que acessam o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio do controle Área de Trabalho Remota ActiveX.

**Para disponibilizar um aplicativo de canal virtual**

1.  Implante o módulo do lado do servidor do aplicativo e certifique-se de que ele está em execução no Host da Sessão RD servidor. Na página de conexão do aplicativo Web Serviços de Área de Trabalho Remota em execução no servidor Web, acesse a propriedade **PluginDlls** da interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) para especificar o nome da DLL do canal virtual. Se você tiver mais de um plug-in, especifique uma lista delimitada por vírgulas de nomes de DLL. Por exemplo, se o plug-in de canal virtual for denominado "MyPlugin.dll", use o seguinte código:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Use o código a seguir se você tiver duas DLLs de canal virtual. Neste exemplo, os nomes de arquivo DLL são "MyPlugin.dll" e "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Por motivos de segurança, a **propriedade PluginDlls** aceita apenas uma lista nomeada de DLLs de canal virtual. O controle retornará um erro se qualquer forma de sistema de arquivos ou caminho UNC for especificado. Além disso, os nomes das DLLs devem conter apenas caracteres alfanuméricos.

2.  Verifique se o módulo do lado do cliente está instalado no diretório %windir% \\ system32.

A API de canal virtual não permite que várias instâncias da mesma DLL de canal virtual sejam carregadas em um único processo. Por isso, se houver várias instâncias do controle Área de Trabalho Remota ActiveX em execução no mesmo processo, somente a primeira instância do controle poderá carregar a DLL do canal virtual. Se você estiver projetando um aplicativo de canal virtual que deve dar suporte a várias instâncias em um único processo, deverá usar a [API](dynamic-virtual-channels.md) de Canais Virtuais Dinâmicos para implementar seu aplicativo de canal virtual.

> [!Note]  
> Por padrão, o controle Área de Trabalho Remota ActiveX carrega DLLs de cliente de canal virtual do diretório %windir% \\ system32. É possível que um administrador altere esse diretório DLL de plug-in de cliente padrão. Para fazer isso, edite a chave do registro **\_ \_** \\  \\  \\  \\ **vdllpath** do cliente do HKEY LOCAL MACHINE Software Microsoft Terminal Server no computador cliente. Esse caminho de diretório não pode ser especificado no formato UNC.

 

 

 




