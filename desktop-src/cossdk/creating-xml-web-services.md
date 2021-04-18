---
description: Qualquer aplicativo COM+ pode ser exposto como um serviço Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Criando Serviços Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796222"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="700c1-103">Criando Serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="700c1-103">Creating XML Web Services</span></span>

<span data-ttu-id="700c1-104">Qualquer aplicativo COM+ pode ser exposto como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="700c1-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="700c1-105">Os métodos nas interfaces padrão dos componentes configurados aplicativos (componentes no catálogo COM+ de servidores) podem ser chamados remotamente.</span><span class="sxs-lookup"><span data-stu-id="700c1-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="700c1-106">Você pode usar a ferramenta administrativa serviços de componentes para criar um diretório raiz virtual do IIS a partir do qual os métodos de componente podem ser chamados usando SOAP.</span><span class="sxs-lookup"><span data-stu-id="700c1-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="700c1-107">O .NET Framework deve ser instalado em seu computador para expor um aplicativo COM+ como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="700c1-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="700c1-108">**Para expor um aplicativo COM+ como um serviço Web XML**</span><span class="sxs-lookup"><span data-stu-id="700c1-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="700c1-109">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.</span><span class="sxs-lookup"><span data-stu-id="700c1-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="700c1-110">Clique com o botão direito do mouse no aplicativo que você deseja expor como um serviço Web XML e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="700c1-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="700c1-111">Clique na guia **ativação** na caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="700c1-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="700c1-112">Marque a caixa de seleção **usa SOAP** .</span><span class="sxs-lookup"><span data-stu-id="700c1-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="700c1-113">Na caixa de texto **Vroot do SOAP** , digite o nome do diretório raiz virtual do IIS do qual os métodos dos componentes podem ser acessados remotamente.</span><span class="sxs-lookup"><span data-stu-id="700c1-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="700c1-114">Observe que uma VRoot SOAP não pode ser um subdiretório de outro diretório VRoot SOAP.</span><span class="sxs-lookup"><span data-stu-id="700c1-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="700c1-115">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="700c1-115">Click **OK**.</span></span>

    <span data-ttu-id="700c1-116">Se você especificar o diretório raiz virtual do IIS como *vroot* e se o nome de domínio totalmente qualificado de seus servidores for *ServerName*, a URL em que o componente é exposto como um serviço Web XML é https://*ServerName* / *vroot*/.</span><span class="sxs-lookup"><span data-stu-id="700c1-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="700c1-117">O diretório correspondente no sistema de arquivos é o \\ Windows \\ System32 \\ com \\ SoapVRoots \\ *vroot* \\ ; O COM+ coloca vários arquivos de configuração e programas ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="700c1-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="700c1-118">Para um serviço Web XML sob carga pesada, talvez você queira ajustar os parâmetros armazenados no arquivo web.config. Para obter informações sobre esse arquivo, consulte a documentação do IIS.</span><span class="sxs-lookup"><span data-stu-id="700c1-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="700c1-119">As configurações de segurança padrão para um aplicativo COM+ exposto como um serviço Web XML diferem dependendo de qual versão do .NET Framework está instalada.</span><span class="sxs-lookup"><span data-stu-id="700c1-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="700c1-120">Se a versão 1,0 estiver instalada, os serviços Web XML não serão seguros por padrão; todas as chamadas são aceitas e nenhuma criptografia é usada.</span><span class="sxs-lookup"><span data-stu-id="700c1-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="700c1-121">Se a versão 1,1 ou posterior estiver instalada, os serviços Web XML serão protegidos por padrão; os chamadores devem ser autenticados e a criptografia é necessária.</span><span class="sxs-lookup"><span data-stu-id="700c1-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="700c1-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="700c1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="700c1-123">Acessando serviços Web XML no modo CAO</span><span class="sxs-lookup"><span data-stu-id="700c1-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="700c1-124">Acessando serviços Web XML no modo WKO</span><span class="sxs-lookup"><span data-stu-id="700c1-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="700c1-125">Visão geral do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="700c1-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="700c1-126">Protegendo serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="700c1-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



