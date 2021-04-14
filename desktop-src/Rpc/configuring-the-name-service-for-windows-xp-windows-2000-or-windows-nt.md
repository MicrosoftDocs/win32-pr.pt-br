---
title: Configurando o serviço de nome
description: A partir do Windows 2000, quando você instala o SDK do Windows, o programa de instalação seleciona automaticamente o Microsoft Locator como o provedor de serviços de nome. Você pode alterar o nome provedor de serviços por meio do painel de controle.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453593"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="4634b-104">Configurando o serviço de nome</span><span class="sxs-lookup"><span data-stu-id="4634b-104">Configuring the Name Service</span></span>

<span data-ttu-id="4634b-105">A partir do Windows 2000, quando você instala o SDK do Windows, o programa de instalação seleciona automaticamente o Microsoft Locator como o provedor de serviços de nome.</span><span class="sxs-lookup"><span data-stu-id="4634b-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="4634b-106">Você pode alterar o nome provedor de serviços por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4634b-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="4634b-107">O computador host que executa o nsid atua como um gateway para o serviço de diretório de célula do DCE, passando chamadas de função de NSI entre computadores que executam sistemas operacionais da Microsoft e computadores DCE.</span><span class="sxs-lookup"><span data-stu-id="4634b-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="4634b-108">Um endereço de rede pode ter até 80 caracteres — por exemplo, 11.1.9.169 é um endereço válido.</span><span class="sxs-lookup"><span data-stu-id="4634b-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="4634b-109">Você deve ter o produto Digital Equipment Corporation DCE CDS para configurar os CDS do DCE como seu provedor de serviços de nome.</span><span class="sxs-lookup"><span data-stu-id="4634b-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="4634b-110">Consulte a documentação fornecida pela Digital Equipment Corporation para obter informações sobre os CDS da DCE.</span><span class="sxs-lookup"><span data-stu-id="4634b-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="4634b-111">**Para reconfigurar o provedor de serviços de nome**</span><span class="sxs-lookup"><span data-stu-id="4634b-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="4634b-112">No painel de controle, clique no ícone **conexões de rede** .</span><span class="sxs-lookup"><span data-stu-id="4634b-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="4634b-113">A janela **conexões de rede** é exibida.</span><span class="sxs-lookup"><span data-stu-id="4634b-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="4634b-114">Selecione a conexão de rede a ser configurada, clique com o botão direito do mouse e selecione **Propriedades** no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="4634b-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="4634b-115">A caixa de diálogo **Propriedades da conexão** é exibida.</span><span class="sxs-lookup"><span data-stu-id="4634b-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="4634b-116">Na caixa de diálogo **Propriedades da conexão** , selecione **cliente para redes Microsoft** e clique no botão **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="4634b-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="4634b-117">A caixa de diálogo **cliente para propriedades de rede da Microsoft** é exibida.</span><span class="sxs-lookup"><span data-stu-id="4634b-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="4634b-118">Na caixa **de diálogo cliente para propriedades de rede da Microsoft** , abra a lista suspensa **provedor de serviços de nome** e selecione um provedor de nomes na listagem.</span><span class="sxs-lookup"><span data-stu-id="4634b-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="4634b-119">Ao selecionar Microsoft Locator, clique em OK.</span><span class="sxs-lookup"><span data-stu-id="4634b-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="4634b-120">O processo de configuração é concluído.</span><span class="sxs-lookup"><span data-stu-id="4634b-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="4634b-121">Ao selecionar o serviço de diretório de célula do DCE, na caixa **endereço de rede** , digite o nome do computador host que executa o daemon NSI (nsid) e clique em OK.</span><span class="sxs-lookup"><span data-stu-id="4634b-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="4634b-122">**Para reconfigurar o provedor de serviços de nome para o Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4634b-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="4634b-123">No painel de controle, clique no ícone de **rede** .</span><span class="sxs-lookup"><span data-stu-id="4634b-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="4634b-124">A caixa de diálogo **rede** é exibida.</span><span class="sxs-lookup"><span data-stu-id="4634b-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="4634b-125">Na caixa de diálogo **rede** , clique em **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="4634b-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="4634b-126">Na lista **NetworkSoftware** , selecione **configuração de RPC**.</span><span class="sxs-lookup"><span data-stu-id="4634b-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="4634b-127">A caixa de diálogo **configuração do provedor de serviço de nome RPC** é exibida.</span><span class="sxs-lookup"><span data-stu-id="4634b-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="4634b-128">Na caixa de diálogo **configuração do provedor de serviço de nome de RPC** , selecione um provedor de serviços de nome na lista.</span><span class="sxs-lookup"><span data-stu-id="4634b-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="4634b-129">Ao selecionar Microsoft Locator, clique em OK.</span><span class="sxs-lookup"><span data-stu-id="4634b-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="4634b-130">O processo de configuração é concluído.</span><span class="sxs-lookup"><span data-stu-id="4634b-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="4634b-131">Ao selecionar o serviço de diretório de célula do DCE, na caixa **endereço de rede** , digite o nome do computador host que executa o daemon NSI (nsid) e clique em OK.</span><span class="sxs-lookup"><span data-stu-id="4634b-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 




