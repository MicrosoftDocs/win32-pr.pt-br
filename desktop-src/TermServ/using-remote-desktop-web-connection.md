---
title: Usando o controle ActiveX Área de Trabalho Remota
description: Como você pode usar o controle ActiveX Área de Trabalho Remota para personalizar a experiência do usuário do Serviços de Área de Trabalho Remota.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando o controle ActiveX do Área de Trabalho Remota
- Conexão Web de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando
- protocolo RDP Serviços de Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788026"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="03282-106">Usando o controle ActiveX Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="03282-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="03282-107">Os tópicos a seguir contêm informações sobre como você pode usar o Área de Trabalho Remota controle ActiveX para personalizar a experiência do usuário do Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="03282-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="03282-108">O controle ActiveX Área de Trabalho Remota está disponível nos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="03282-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="03282-109">**O controle programável**— implementa interfaces que são seguras para scripts.</span><span class="sxs-lookup"><span data-stu-id="03282-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="03282-110">Essa forma do controle pode ser usada por clientes da Web ou scripts (como VBScript) hosts.</span><span class="sxs-lookup"><span data-stu-id="03282-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="03282-111">**O controle não programável**— oferece funcionalidade adicional que não é segura para scripts.</span><span class="sxs-lookup"><span data-stu-id="03282-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="03282-112">Essa forma do controle pode ser usada a partir de código nativo ou gerenciado, mas esse formulário não pode ser usado por clientes Web ou hosts somente de script.</span><span class="sxs-lookup"><span data-stu-id="03282-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="03282-113">A lista a seguir contém os s do **CLSID** para os diferentes controles para diferentes versões do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="03282-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="03282-114">Cada um dos **CLSID** s é compatível com versões posteriores do sistema.</span><span class="sxs-lookup"><span data-stu-id="03282-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="03282-115">Por exemplo, o **CLSID** para o controle programável no Windows Vista funcionará em versões posteriores do sistema, como o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03282-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="03282-116">Versão do sistema</span><span class="sxs-lookup"><span data-stu-id="03282-116">System version</span></span>                          | <span data-ttu-id="03282-117">CLSID de controle programável</span><span class="sxs-lookup"><span data-stu-id="03282-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="03282-118">CLSID de controle não programável</span><span class="sxs-lookup"><span data-stu-id="03282-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="03282-119">Windows 8.1, Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="03282-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="03282-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="03282-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="03282-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="03282-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="03282-122">Windows 8, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03282-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="03282-123">5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="03282-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="03282-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="03282-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="03282-125">Windows 7, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03282-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="03282-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="03282-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="03282-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="03282-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="03282-128">Windows Vista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="03282-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="03282-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="03282-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="03282-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="03282-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="03282-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03282-131">Windows Vista</span></span>                           | <span data-ttu-id="03282-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="03282-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="03282-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="03282-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="03282-134">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="03282-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="03282-135">Inserindo o controle ActiveX Área de Trabalho Remota em uma página da Web</span><span class="sxs-lookup"><span data-stu-id="03282-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="03282-136">Exemplo que demonstra o uso das interfaces programáveis.</span><span class="sxs-lookup"><span data-stu-id="03282-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="03282-137">Implementando canais virtuais programáveis usando o Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="03282-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="03282-138">Exemplos de código que mostram as etapas para implementar canais virtuais programáveis com Conexão Web de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="03282-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="03282-139">Usando o controle ActiveX Área de Trabalho Remota com canais virtuais</span><span class="sxs-lookup"><span data-stu-id="03282-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="03282-140">Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para os computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="03282-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="03282-141">Página da Web de exemplo incluída com o controle ActiveX Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="03282-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="03282-142">Uma página da Web de exemplo (Default.htm) está no diretório onde Conexão Web de Área de Trabalho Remota está instalado.</span><span class="sxs-lookup"><span data-stu-id="03282-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="03282-143">Fornecendo para o RDP Client Security</span><span class="sxs-lookup"><span data-stu-id="03282-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="03282-144">Algumas propriedades do objeto de controle ActiveX Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="03282-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="03282-145">Desabilitando recursos de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="03282-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="03282-146">Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos.</span><span class="sxs-lookup"><span data-stu-id="03282-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="03282-147">Para obter mais informações sobre a página da Web de exemplo incluída na instalação do controle ActiveX Área de Trabalho Remota, consulte a [página da Web de exemplo incluída com o controle activex área de trabalho remota](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="03282-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




