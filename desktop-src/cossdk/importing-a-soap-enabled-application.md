---
description: Quando um aplicativo habilitado para SOAP é exportado de um servidor no modo proxy, os clientes que o importam podem acessar automaticamente os métodos dos componentes que ele contém, remotamente, como serviços Web oferecidos pelo servidor no modo CAO (objeto ativado pelo cliente). Isso permite que você implante com facilidade a funcionalidade de um aplicativo COM+ em uma rede como um serviço Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importando um aplicativo SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501087"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="311ee-104">Importando um aplicativo SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="311ee-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="311ee-105">Quando um aplicativo habilitado para SOAP é [exportado](exporting-a-soap-enabled-application.md) de um servidor no modo proxy, os clientes que o importam podem acessar automaticamente os métodos dos componentes que ele contém, remotamente, como serviços Web oferecidos pelo servidor no modo Cao (objeto ativado pelo cliente).</span><span class="sxs-lookup"><span data-stu-id="311ee-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="311ee-106">Isso permite que você implante com facilidade a funcionalidade de um aplicativo COM+ em uma rede como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="311ee-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="311ee-107">Quando os componentes de um aplicativo importados dessa maneira são usados no cliente, eles não são executados no cliente, mas, em vez disso, são acessados remotamente usando o serviço Web XML fornecido pelo servidor do qual o aplicativo foi exportado.</span><span class="sxs-lookup"><span data-stu-id="311ee-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="311ee-108">Para obter detalhes sobre como usar os componentes de um aplicativo importado dessa forma, consulte [acessando serviços Web XML no modo Cao](accessing-xml-web-services-in-cao-mode.md).</span><span class="sxs-lookup"><span data-stu-id="311ee-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="311ee-109">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="311ee-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="311ee-110">Para importar um aplicativo habilitado para SOAP em um cliente, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="311ee-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="311ee-111">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta associada ao computador cliente no qual você deseja instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="311ee-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="311ee-112">Clique com o botão direito do mouse na pasta **aplicativos com+** do cliente e escolha **novo**.</span><span class="sxs-lookup"><span data-stu-id="311ee-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="311ee-113">O **Assistente de instalação do aplicativo com+** é exibido.</span><span class="sxs-lookup"><span data-stu-id="311ee-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="311ee-114">No **Assistente de instalação de aplicativo com+**, clique em **instalar aplicativos pré-criados**.</span><span class="sxs-lookup"><span data-stu-id="311ee-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="311ee-115">Procure a rede para localizar ou especificar o caminho de rede do arquivo MSI no servidor do qual você deseja instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="311ee-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="311ee-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="311ee-116">Visual Basic</span></span>

<span data-ttu-id="311ee-117">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="311ee-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="311ee-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="311ee-118">C/C++</span></span>

<span data-ttu-id="311ee-119">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="311ee-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="311ee-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="311ee-120">Remarks</span></span>

<span data-ttu-id="311ee-121">Os componentes COM são identificados por um GUID, que altera se os componentes são recompilados.</span><span class="sxs-lookup"><span data-stu-id="311ee-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="311ee-122">Se um componente COM configurado que é exposto como um serviço Web XML for recompilado, os aplicativos cliente que o utilizam serão interrompidos.</span><span class="sxs-lookup"><span data-stu-id="311ee-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="311ee-123">Portanto, quando um componente exposto como um serviço Web XML é recompilado, os clientes devem importar novamente os aplicativos que usam o componente.</span><span class="sxs-lookup"><span data-stu-id="311ee-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="311ee-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="311ee-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="311ee-125">Visão geral do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="311ee-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="311ee-126">Criando Serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="311ee-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="311ee-127">Exportando um aplicativo SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="311ee-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



