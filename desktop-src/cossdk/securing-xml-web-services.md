---
description: O acesso a aplicativos COM+ expostos como XML Web Services é controlado pelo servidor Web do IIS, que processa as solicitações de entrada.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Protegendo serviços Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812150"
---
# <a name="securing-xml-web-services"></a><span data-ttu-id="44194-103">Protegendo serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="44194-103">Securing XML Web Services</span></span>

<span data-ttu-id="44194-104">O acesso a aplicativos COM+ expostos como XML Web Services é controlado pelo servidor Web do IIS, que processa as solicitações de entrada.</span><span class="sxs-lookup"><span data-stu-id="44194-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="44194-105">Você também pode configurar o IIS para exigir que as comunicações com o chamador ocorram em um canal seguro estabelecido usando o protocolo protocolo SSL (SSL).</span><span class="sxs-lookup"><span data-stu-id="44194-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="44194-106">Um serviço Web XML seguro não dá suporte ao acesso WKO via WSDL.</span><span class="sxs-lookup"><span data-stu-id="44194-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="44194-107">Em vez disso, os clientes que instalaram a versão 1,1 do .NET Framework podem chamá-lo no modo CAO.</span><span class="sxs-lookup"><span data-stu-id="44194-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="44194-108">Se os clientes de terceiros precisarem acessar o serviço Web XML via WSDL, você deverá permitir o acesso anônimo.</span><span class="sxs-lookup"><span data-stu-id="44194-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="44194-109">Para usar o protocolo SSL para estabelecer um canal de comunicação seguro, você deve obter e instalar um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="44194-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="44194-110">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="44194-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="44194-111">Para selecionar o mecanismo de autenticação para um serviço Web XML, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="44194-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="44194-112">Clique com o botão direito do mouse no ícone de **meu computador** na área de trabalho e clique em **gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="44194-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="44194-113">Em **serviços e aplicativos** e **serviço de informações da Internet**, localize o ícone correspondente ao diretório raiz virtual do seu serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="44194-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="44194-114">Clique com o botão direito do mouse no ícone de diretório e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="44194-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="44194-115">Na guia **segurança de diretório** da caixa de diálogo Propriedades, localize **autenticação e controle de acesso** e clique no botão **Editar** correspondente.</span><span class="sxs-lookup"><span data-stu-id="44194-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="44194-116">Na caixa de diálogo **métodos de autenticação** , em **acesso autenticado**, use as caixas de seleção para selecionar os mecanismos de autenticação que deseja permitir.</span><span class="sxs-lookup"><span data-stu-id="44194-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="44194-117">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="44194-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="44194-118">Você pode configurar o IIS para autenticar chamadores usando qualquer uma das seguintes opções na caixa de diálogo **métodos de autenticação** do IIS: **autenticação integrada do Windows**, **autenticação Digest para servidores de domínio do Windows**, **autenticação básica (senha enviada em texto não criptografado)** ou **autenticação do .NET Passport**.</span><span class="sxs-lookup"><span data-stu-id="44194-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="44194-119">Você também pode permitir o acesso anônimo.</span><span class="sxs-lookup"><span data-stu-id="44194-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="44194-120">Na caixa de diálogo Propriedades, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="44194-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="44194-121">Para permitir acesso não seguro e anônimo a um serviço Web XML, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="44194-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="44194-122">Clique com o botão direito do mouse no ícone de **meu computador** na área de trabalho e clique em **gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="44194-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="44194-123">Em **serviços e aplicativos** e **serviço de informações da Internet**, localize o ícone correspondente ao diretório raiz virtual do seu serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="44194-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="44194-124">Clique com o botão direito do mouse no ícone de diretório e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="44194-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="44194-125">Na guia **segurança de diretório** da caixa de diálogo Propriedades, localize **autenticação e controle de acesso** e clique no botão **Editar** correspondente.</span><span class="sxs-lookup"><span data-stu-id="44194-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="44194-126">Marque a caixa de seleção **habilitar acesso anônimo** .</span><span class="sxs-lookup"><span data-stu-id="44194-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="44194-127">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="44194-127">Click **OK**.</span></span>

4.  <span data-ttu-id="44194-128">Na guia **segurança de diretório** da caixa de diálogo Propriedades, localize **comunicações seguras** e clique no botão **Editar** correspondente.</span><span class="sxs-lookup"><span data-stu-id="44194-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="44194-129">Desmarque a caixa de seleção **exigir canal seguro (SSL)** .</span><span class="sxs-lookup"><span data-stu-id="44194-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="44194-130">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="44194-130">Click **OK**.</span></span>

5.  <span data-ttu-id="44194-131">Na caixa de diálogo Propriedades, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="44194-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="44194-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="44194-132">Visual Basic</span></span>

<span data-ttu-id="44194-133">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="44194-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="44194-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="44194-134">C/C++</span></span>

<span data-ttu-id="44194-135">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="44194-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="44194-136">Considerações adicionais sobre segurança</span><span class="sxs-lookup"><span data-stu-id="44194-136">Additional Security Considerations</span></span>

<span data-ttu-id="44194-137">Ao exigir um canal seguro, você ajuda a proteger a confidencialidade dos dados trocados criptografando as comunicações entre o cliente e o serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="44194-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="44194-138">Se você permitir a autenticação usando senhas de texto não criptografado, precisará de um canal seguro para evitar a exposição de senhas na rede.</span><span class="sxs-lookup"><span data-stu-id="44194-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44194-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44194-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44194-140">Acessando serviços Web XML no modo CAO</span><span class="sxs-lookup"><span data-stu-id="44194-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="44194-141">Acessando serviços Web XML no modo WKO</span><span class="sxs-lookup"><span data-stu-id="44194-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="44194-142">Considerações de segurança do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="44194-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="44194-143">Criando Serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="44194-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 



