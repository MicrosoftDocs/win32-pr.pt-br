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
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="9dd2e-103">Usando o controle ActiveX Área de Trabalho Remota com canais virtuais</span><span class="sxs-lookup"><span data-stu-id="9dd2e-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="9dd2e-104">Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para os computadores cliente que acessam o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio do controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="9dd2e-105">**Para disponibilizar um aplicativo de canal virtual**</span><span class="sxs-lookup"><span data-stu-id="9dd2e-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="9dd2e-106">Implante o módulo do lado do servidor do aplicativo e verifique se ele está em execução no servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="9dd2e-107">Na página conexão do aplicativo Web Serviços de Área de Trabalho Remota em execução no servidor Web, acesse a propriedade **PluginDlls** da interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) para especificar o nome da sua DLL de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="9dd2e-108">Se você tiver mais de um plug-in, especifique uma lista delimitada por vírgulas de nomes de DLL.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="9dd2e-109">Por exemplo, se o seu plug-in de canal virtual for nomeado "MyPlugin.dll", use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="9dd2e-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="9dd2e-110">Use o código a seguir se você tiver duas DLLs de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="9dd2e-111">Neste exemplo, os nomes de arquivo DLL são "MyPlugin.dll" e "Vdriver.dll":</span><span class="sxs-lookup"><span data-stu-id="9dd2e-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="9dd2e-112">Por motivos de segurança, a propriedade **PluginDlls** aceita apenas uma lista nomeada de DLLs de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="9dd2e-113">O controle retornará um erro se qualquer forma de sistema de arquivos ou caminho UNC for especificada.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="9dd2e-114">Além disso, os nomes das DLLs devem conter apenas caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="9dd2e-115">Verifique se o módulo do lado do cliente está instalado no diretório% windir% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="9dd2e-116">A API de canal virtual não permite que várias instâncias da mesma DLL de canal virtual sejam carregadas em um único processo.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="9dd2e-117">Por isso, se houver várias instâncias do Área de Trabalho Remota controle ActiveX em execução dentro do mesmo processo, somente a primeira instância do controle poderá carregar a DLL do canal virtual.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="9dd2e-118">Se você estiver criando um aplicativo de canal virtual que deve dar suporte a várias instâncias em um único processo, deverá usar a API de [canais virtuais dinâmicos](dynamic-virtual-channels.md) para implementar seu aplicativo de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="9dd2e-119">Por padrão, o controle ActiveX Área de Trabalho Remota carrega as DLLs de cliente do canal virtual do diretório% windir% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="9dd2e-120">É possível que um administrador altere esse diretório de DLL de plug-in de cliente padrão.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="9dd2e-121">Para fazer isso, edite a chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="9dd2e-122">Este caminho de diretório não pode ser especificado no formato UNC.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 




