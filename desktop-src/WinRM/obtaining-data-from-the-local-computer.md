---
title: Obtendo dados do computador local
description: Embora Gerenciamento Remoto do Windows e WS-Management protocolo sejam explicitamente projetados para comunicação remota, o estabelecimento de uma sessão no computador local é o caso mais simples.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641126"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="4628e-103">Obtendo dados do computador local</span><span class="sxs-lookup"><span data-stu-id="4628e-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="4628e-104">Embora Gerenciamento Remoto do Windows e WS-Management protocolo sejam explicitamente projetados para comunicação remota, o estabelecimento de uma sessão no computador local é o caso mais simples.</span><span class="sxs-lookup"><span data-stu-id="4628e-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="4628e-105">Alguns scripts podem exigir acesso aos dados no computador local, bem como em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="4628e-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="4628e-106">**WinRM versão 2,0:  **</span><span class="sxs-lookup"><span data-stu-id="4628e-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="4628e-107">Todas as operações são consideradas remotas e o serviço WinRM deve ser iniciado antes de qualquer operação ser executada.</span><span class="sxs-lookup"><span data-stu-id="4628e-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="4628e-108">Se um destino remoto não for especificado, o localhost será usado por padrão e todas as operações serão enviadas para o serviço WinRM local.</span><span class="sxs-lookup"><span data-stu-id="4628e-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="4628e-109">Para obter mais informações sobre como iniciar o serviço WinRM, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="4628e-110">Ao usar o serviço WinRM para operações locais, os seguintes fatores devem ser considerados:</span><span class="sxs-lookup"><span data-stu-id="4628e-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="4628e-111">A configuração local do WinRM só pode ser lida por administradores.</span><span class="sxs-lookup"><span data-stu-id="4628e-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="4628e-112">Os namespaces do WMI devem ter permissões de habilitação remota definidas.</span><span class="sxs-lookup"><span data-stu-id="4628e-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="4628e-113">Para obter mais informações, consulte [protegendo uma conexão WMI remota](../wmisdk/securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="4628e-114">Se um [*ouvinte*](windows-remote-management-glossary.md) do WinRM não for criado, o serviço WinRM escutará solicitações locais na porta 47001.</span><span class="sxs-lookup"><span data-stu-id="4628e-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="4628e-115">Cada script do WinRM deve começar estabelecendo uma sessão ou conexão com um computador criando um objeto de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="4628e-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="4628e-116">Depois que a sessão é criada, você pode usar os métodos de objeto de **sessão** , como [**Session. enumera**](session-enumerate.md) ou [**Session. Invoke**](session-invoke.md) para obter dados ou para executar métodos.</span><span class="sxs-lookup"><span data-stu-id="4628e-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="4628e-117">A criação de uma sessão é um pouco semelhante à [conexão](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) com um namespace Instrumentação de gerenciamento do Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page)).</span><span class="sxs-lookup"><span data-stu-id="4628e-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="4628e-118">A sessão é essencialmente uma camada que permite que você envie e receba dados por meio de mensagens [*SOAP*](windows-remote-management-glossary.md) e do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="4628e-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="4628e-119">Para obter mais informações, consulte [protocolo WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="4628e-120">Chamar o método [**WSMan. CreateSession**](wsman-createsession.md) para criar um objeto de [**sessão**](session.md) iniciará uma [*sessão*](windows-remote-management-glossary.md) que se conecta ao WinRM local.</span><span class="sxs-lookup"><span data-stu-id="4628e-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="4628e-121">**Para criar uma sessão do WSMan e obter dados**</span><span class="sxs-lookup"><span data-stu-id="4628e-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="4628e-122">Crie um objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="4628e-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="4628e-123">Crie uma sessão chamando o método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="4628e-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="4628e-124">Essa sessão é executada sob seu nome de usuário e senha de logon e pode obter dados por meio do WinRM local.</span><span class="sxs-lookup"><span data-stu-id="4628e-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="4628e-125">Crie um [*URI*](windows-remote-management-glossary.md) de recurso para identificar o [*recurso*](windows-remote-management-glossary.md) que você deseja gerenciar ou para o qual deseja obter dados.</span><span class="sxs-lookup"><span data-stu-id="4628e-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="4628e-126">Para obter mais informações sobre como formatar um URI, consulte [URIs de recurso](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="4628e-127">Esse URI de recurso é para uma instância específica da classe [**de \_ serviço WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) , o serviço Winmgmt.</span><span class="sxs-lookup"><span data-stu-id="4628e-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="4628e-128">Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="4628e-129">Chamar métodos de [**sessão**](session.md) que obtêm ou enumeram dados usando o URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="4628e-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="4628e-130">Para obter mais informações, consulte [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="4628e-131">Para obter ou gerenciar dados de outro computador ou usar métodos diferentes de autenticação, consulte [obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="4628e-132">O exemplo de código VBScript a seguir mostra o script completo que obtém a instância específica do [**\_ serviço WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) chamado "winmgmt".</span><span class="sxs-lookup"><span data-stu-id="4628e-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="4628e-133">O exemplo de código VBScript a seguir mostra o script completo com a transformação de dados.</span><span class="sxs-lookup"><span data-stu-id="4628e-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="4628e-134">Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="4628e-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="4628e-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4628e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4628e-136">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="4628e-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4628e-137">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="4628e-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4628e-138">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="4628e-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 