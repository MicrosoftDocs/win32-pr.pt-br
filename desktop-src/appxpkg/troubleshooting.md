---
title: Solucionar problemas de empacotamento, implantação e consulta de aplicativos Windows
description: Use essas sugestões para solucionar problemas que você enfrenta ao empacotar, implantar ou consultar um pacote de aplicativo.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2021
ms.locfileid: "105810806"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="d4891-103">Solucionar problemas de empacotamento, implantação e consulta de aplicativos Windows</span><span class="sxs-lookup"><span data-stu-id="d4891-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="d4891-104">Use essas sugestões para solucionar problemas que você enfrenta ao empacotar, implantar ou consultar um pacote de aplicativo do Windows (. msix/. AppX) como desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="d4891-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="d4891-105">Este artigo destina-se a desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="d4891-105">This article is intended for developers.</span></span> <span data-ttu-id="d4891-106">Se você não for um desenvolvedor e estiver procurando ajuda com um erro de instalação de aplicativo do Windows, consulte [suporte do Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span><span class="sxs-lookup"><span data-stu-id="d4891-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="d4891-107">Obter informações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="d4891-107">Get diagnostic information</span></span>

<span data-ttu-id="d4891-108">Quando uma API falha, ela retorna um código de erro que descreve o problema.</span><span class="sxs-lookup"><span data-stu-id="d4891-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="d4891-109">Se o código de erro não fornecer informações suficientes, você encontrará mais informações de diagnóstico nos logs de eventos detalhados.</span><span class="sxs-lookup"><span data-stu-id="d4891-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="d4891-110">Para acessar os logs de eventos de empacotamento e implantação usando **Visualizador de eventos**, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4891-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="d4891-111">Execute uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d4891-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="d4891-112">Clique em **Iniciar** no menu Windows, digite **Visualizador de eventos** e **pressione Enter**.</span><span class="sxs-lookup"><span data-stu-id="d4891-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="d4891-113">Execute **eventvwr. msc**.</span><span class="sxs-lookup"><span data-stu-id="d4891-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="d4891-114">Na página esquerda, expanda **Visualizador de eventos (local)**  >  **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**.</span><span class="sxs-lookup"><span data-stu-id="d4891-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="d4891-115">Verifique os logs disponíveis nessas categorias:</span><span class="sxs-lookup"><span data-stu-id="d4891-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="d4891-116">**AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/operacional**</span><span class="sxs-lookup"><span data-stu-id="d4891-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="d4891-117">**AppXDeployment-servidor**  >  **Microsoft-Windows-AppXDeploymentServer/operacional**</span><span class="sxs-lookup"><span data-stu-id="d4891-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="d4891-118">Comece examinando os logs em **AppXDeployment-Server**.</span><span class="sxs-lookup"><span data-stu-id="d4891-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="d4891-119">Se o erro foi causado por **0x80073CF0** ou **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, detalhes adicionais podem estar presentes nos logs do **AppxpackagingOM** .</span><span class="sxs-lookup"><span data-stu-id="d4891-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="d4891-120">Você também pode usar o comando [Get-AppxLog](/powershell/module/appx/get-appxlog) no PowerShell para obter os primeiros eventos registrados.</span><span class="sxs-lookup"><span data-stu-id="d4891-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="d4891-121">O exemplo a seguir exibe os logs associados à operação de implantação mais recente.</span><span class="sxs-lookup"><span data-stu-id="d4891-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="d4891-122">O exemplo a seguir exibe os logs associados à operação de implantação mais recente em uma tabela interativa em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="d4891-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="d4891-123">Códigos de erro comuns</span><span class="sxs-lookup"><span data-stu-id="d4891-123">Common error codes</span></span>

<span data-ttu-id="d4891-124">Esta tabela lista alguns dos códigos de erro mais comuns.</span><span class="sxs-lookup"><span data-stu-id="d4891-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="d4891-125">Se você precisar de ajuda adicional com um desses erros, ou se estiver encontrando um código de erro que não esteja nessa lista, consulte [Opções de ajuda adicionais](#get-additional-help).</span><span class="sxs-lookup"><span data-stu-id="d4891-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4891-126">Código do erro</span><span class="sxs-lookup"><span data-stu-id="d4891-126">Error code</span></span></th>
<th><span data-ttu-id="d4891-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d4891-127">Value</span></span></th>
<th><span data-ttu-id="d4891-128">Descrição e possíveis causas</span><span class="sxs-lookup"><span data-stu-id="d4891-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="d4891-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="d4891-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="d4891-130">0x80070002</span></span></td>
<td><span data-ttu-id="d4891-131">Arquivo ou caminho não encontrado.</span><span class="sxs-lookup"><span data-stu-id="d4891-131">File or path is not found.</span></span> <span data-ttu-id="d4891-132">Isso pode ocorrer durante uma validação de typelib COM e requer que o caminho para o diretório realmente exista no pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="d4891-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="d4891-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="d4891-134">0x8007000B</span></span></td>
<td><span data-ttu-id="d4891-135">O pacote não está formatado corretamente e deve ser recompilado ou assinado novamente.</span><span class="sxs-lookup"><span data-stu-id="d4891-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="d4891-136">Você poderá receber esse erro se houver uma incompatibilidade entre o nome da entidade do certificado de autenticação e o nome do editor de AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d4891-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="d4891-137">Consulte <a href="how-to-sign-a-package-using-signtool.md">como assinar um pacote de aplicativo usando Signtool</a>.</span><span class="sxs-lookup"><span data-stu-id="d4891-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="d4891-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="d4891-139">0x80070057</span></span></td>
<td><span data-ttu-id="d4891-140">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="d4891-140">One or more arguments are not valid.</span></span> <span data-ttu-id="d4891-141">Se você verificar o log de eventos AppXDeployment-Server e vir o seguinte evento: "durante a instalação do pacote, o sistema não pôde registrar a extensão Windows. repositoryExtension devido ao seguinte erro: o parâmetro está incorreto".</span><span class="sxs-lookup"><span data-stu-id="d4891-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="d4891-142">Você poderá receber esse erro se o DisplayName ou a descrição dos elementos do manifesto contiverem caracteres não permitidos pelo firewall do Windows; a saber |  e todos, devido ao que o Windows falha ao criar o perfil do AppContainer para o pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="d4891-143">Remova esses caracteres do manifesto e tente instalar o pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="d4891-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="d4891-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="d4891-147">Não foi possível abrir o pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="d4891-148">Possíveis causas:</span><span class="sxs-lookup"><span data-stu-id="d4891-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="d4891-149">O pacote não está assinado.</span><span class="sxs-lookup"><span data-stu-id="d4891-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="d4891-150">O nome do editor não corresponde ao assunto do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d4891-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="d4891-151">O prefixo file://está ausente ou o pacote não pôde ser encontrado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="d4891-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="d4891-152">Para obter mais informações, verifique o log de eventos <strong>AppxPackagingOM</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-155">0x80073CF1</span><span class="sxs-lookup"><span data-stu-id="d4891-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="d4891-156">Não foi possível encontrar o pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="d4891-157">Você pode receber esse erro ao remover um pacote que não está instalado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d4891-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-159"><strong>AGRUPA</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-160">0x80073CF2</span><span class="sxs-lookup"><span data-stu-id="d4891-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="d4891-161">Os dados do pacote não são válidos.</span><span class="sxs-lookup"><span data-stu-id="d4891-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="d4891-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="d4891-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="d4891-165">Falha na atualização do pacote, dependência ou validação de conflito.</span><span class="sxs-lookup"><span data-stu-id="d4891-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="d4891-166">Possíveis causas:</span><span class="sxs-lookup"><span data-stu-id="d4891-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="d4891-167">O pacote de entrada está em conflito com um pacote instalado.</span><span class="sxs-lookup"><span data-stu-id="d4891-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="d4891-168">Uma dependência de pacote especificada não pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="d4891-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="d4891-169">O pacote não dá suporte à arquitetura de processador correta.</span><span class="sxs-lookup"><span data-stu-id="d4891-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="d4891-170">Para obter mais informtion, verifique o log de eventos <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="d4891-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-173">0x80073CF4</span><span class="sxs-lookup"><span data-stu-id="d4891-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="d4891-174">Não há espaço em disco suficiente no computador.</span><span class="sxs-lookup"><span data-stu-id="d4891-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="d4891-175">Libere algum espaço e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="d4891-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="d4891-177"><strong>FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-178">0x80073CF5</span><span class="sxs-lookup"><span data-stu-id="d4891-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="d4891-179">O pacote não pode ser baixado.</span><span class="sxs-lookup"><span data-stu-id="d4891-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="d4891-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-182">0x80073CF6</span><span class="sxs-lookup"><span data-stu-id="d4891-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="d4891-183">O pacote não pode ser registrado.</span><span class="sxs-lookup"><span data-stu-id="d4891-183">The package can't be registered.</span></span><br/> <span data-ttu-id="d4891-184">Para obter mais informações, verifique o log de eventos <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="d4891-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-187">0x80073CF7</span><span class="sxs-lookup"><span data-stu-id="d4891-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="d4891-188">Não é possível cancelar o registro do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="d4891-189">Você pode receber esse erro ao remover um pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="d4891-190">Para obter mais informações, verifique o log de eventos <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="d4891-192">0x80073CF8</span><span class="sxs-lookup"><span data-stu-id="d4891-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="d4891-193">O usuário cancelou a solicitação de instalação.</span><span class="sxs-lookup"><span data-stu-id="d4891-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="d4891-195">0x80073CF9</span><span class="sxs-lookup"><span data-stu-id="d4891-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="d4891-196">Falha na instalação do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-196">Package install failed.</span></span> <span data-ttu-id="d4891-197">Contate o fornecedor do software.</span><span class="sxs-lookup"><span data-stu-id="d4891-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="d4891-198">Para obter mais informações, verifique o log de eventos <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="d4891-200">0x80073CFA</span><span class="sxs-lookup"><span data-stu-id="d4891-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="d4891-201">Falha na remoção do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-201">Package removal failed.</span></span><br/> <span data-ttu-id="d4891-202">Você pode receber esse erro para falhas que ocorrem durante a desinstalação do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="d4891-203">Para obter mais informações, consulte <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d4891-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="d4891-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="d4891-207">O pacote fornecido já foi instalado e sua reinstalação está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="d4891-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="d4891-208">Você poderá receber esse erro se estiver instalando um pacote que não seja um bit idêntico ao pacote que já está instalado.</span><span class="sxs-lookup"><span data-stu-id="d4891-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="d4891-209">Observe que a assinatura digital também faz parte do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="d4891-210">Portanto, se um pacote for recriado ou assinado, ele não será mais idêntico a bit que o pacote instalado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d4891-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="d4891-211">Duas opções possíveis para corrigir esse erro são: (1) incrementar o número de versão do aplicativo e, em seguida, recompilar e desistir do pacote (2) remover o pacote antigo para cada usuário no sistema antes de instalar o novo pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="d4891-213">0x80073CFC</span><span class="sxs-lookup"><span data-stu-id="d4891-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="d4891-214">O aplicativo não pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="d4891-214">The app can't be started.</span></span> <span data-ttu-id="d4891-215">Tente reinstalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4891-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="d4891-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-218">0x80073CFD</span><span class="sxs-lookup"><span data-stu-id="d4891-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="d4891-219">Um pré-requisito de instalação especificado não pôde ser atendido.</span><span class="sxs-lookup"><span data-stu-id="d4891-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-222">0x80073CFE</span><span class="sxs-lookup"><span data-stu-id="d4891-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="d4891-223">O repositório do pacote está corrompido.</span><span class="sxs-lookup"><span data-stu-id="d4891-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="d4891-224">Você poderá receber esse erro se a pasta referenciada por essa chave do registro não existir ou estiver corrompida:</span><span class="sxs-lookup"><span data-stu-id="d4891-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="d4891-225"><strong>HKLM\Software\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="d4891-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="d4891-227">Para se recuperar desse Estado, atualize seu computador.</span><span class="sxs-lookup"><span data-stu-id="d4891-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="d4891-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="d4891-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="d4891-231">Para instalar esse aplicativo, você precisa de uma licença de desenvolvedor ou um sistema habilitado para Sideload.</span><span class="sxs-lookup"><span data-stu-id="d4891-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="d4891-232">Você poderá receber esse erro se o pacote não atender a um dos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="d4891-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="d4891-233">O aplicativo é implantado usando F5 no Visual Studio em um computador com uma licença de desenvolvedor do Windows.</span><span class="sxs-lookup"><span data-stu-id="d4891-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="d4891-234">O pacote é assinado com uma assinatura da Microsoft e implantado como parte do Windows ou do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d4891-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="d4891-235">O pacote é assinado com uma assinatura confiável e instalado em um computador com uma licença de desenvolvedor, um computador ingressado no domínio com a política AllowAllTrustedApps habilitada ou um computador com uma licença de Sideload do Windows com a política AllowAllTrustedApps habilitada.</span><span class="sxs-lookup"><span data-stu-id="d4891-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="d4891-237">0x80073D00</span><span class="sxs-lookup"><span data-stu-id="d4891-237">0x80073D00</span></span></td>
<td><span data-ttu-id="d4891-238">O aplicativo não pode ser iniciado porque está sendo atualizado no momento.</span><span class="sxs-lookup"><span data-stu-id="d4891-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="d4891-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-241">0x80073D01</span><span class="sxs-lookup"><span data-stu-id="d4891-241">0x80073D01</span></span></td>
<td><span data-ttu-id="d4891-242">A operação de implantação de pacote está bloqueada pela política.</span><span class="sxs-lookup"><span data-stu-id="d4891-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="d4891-243">Entre em contato com o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="d4891-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="d4891-244">Possíveis causas:</span><span class="sxs-lookup"><span data-stu-id="d4891-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="d4891-245">A implantação de pacote é bloqueada pelas políticas de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4891-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="d4891-246">A implantação do pacote é bloqueada pela &quot; política permitir implantação em perfis especiais &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4891-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="d4891-247">Um dos motivos possíveis é a necessidade de um perfil móvel.</span><span class="sxs-lookup"><span data-stu-id="d4891-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="d4891-248">Para obter informações sobre como configurar perfis de usuário móvel em contas de usuário, consulte <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">implantar perfis de usuário de roaming</a>.</span><span class="sxs-lookup"><span data-stu-id="d4891-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="d4891-249">Se não houver políticas configuradas no seu sistema e você ainda vir esse erro, talvez você esteja conectado com um perfil temporário.</span><span class="sxs-lookup"><span data-stu-id="d4891-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="d4891-250">Faça logoff e logon novamente e tente a operação novamente.</span><span class="sxs-lookup"><span data-stu-id="d4891-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="d4891-252">0x80073D02</span><span class="sxs-lookup"><span data-stu-id="d4891-252">0x80073D02</span></span></td>
<td><span data-ttu-id="d4891-253">Não foi possível instalar o pacote porque os recursos que ele modifica estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="d4891-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="d4891-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-256">0x80073D03</span><span class="sxs-lookup"><span data-stu-id="d4891-256">0x80073D03</span></span></td>
<td><span data-ttu-id="d4891-257">Não foi possível recuperar o pacote porque os dados necessários para a recuperação estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="d4891-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-260">0x80073D04</span><span class="sxs-lookup"><span data-stu-id="d4891-260">0x80073D04</span></span></td>
<td><span data-ttu-id="d4891-261">A assinatura não é válida.</span><span class="sxs-lookup"><span data-stu-id="d4891-261">The signature isn't valid.</span></span> <span data-ttu-id="d4891-262">Para se registrar no modo de desenvolvedor, AppxSignature. P7X e AppxBlockMap.xml devem ser válidos ou não devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="d4891-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="d4891-263">Se você for um desenvolvedor usando F5 com o Visual Studio, verifique se o diretório do projeto criado não contém arquivos de mapa de assinatura ou de bloco de versões anteriores do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="d4891-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-266">0x80073D05</span><span class="sxs-lookup"><span data-stu-id="d4891-266">0x80073D05</span></span></td>
<td><span data-ttu-id="d4891-267">Ocorreu um erro ao excluir os dados de aplicativo anteriormente existentes do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="d4891-268">Você pode obter esse erro se o <a href="/previous-versions/hh441475(v=vs.110)">simulador</a> estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="d4891-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="d4891-269">Feche o simulador.</span><span class="sxs-lookup"><span data-stu-id="d4891-269">Close the simulator.</span></span> <span data-ttu-id="d4891-270">Você também pode obter esse erro se houver arquivos abertos nos dados do aplicativo (por exemplo, se você tiver um arquivo de log aberto em um editor de texto).</span><span class="sxs-lookup"><span data-stu-id="d4891-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="d4891-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-273">0x80073D06</span><span class="sxs-lookup"><span data-stu-id="d4891-273">0x80073D06</span></span></td>
<td><span data-ttu-id="d4891-274">Não foi possível instalar o pacote porque uma versão mais recente deste pacote já está instalada.</span><span class="sxs-lookup"><span data-stu-id="d4891-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="d4891-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-277">0x80073D07</span><span class="sxs-lookup"><span data-stu-id="d4891-277">0x80073D07</span></span></td>
<td><span data-ttu-id="d4891-278">Foi detectado um erro em um binário do sistema.</span><span class="sxs-lookup"><span data-stu-id="d4891-278">An error in a system binary was detected.</span></span> <span data-ttu-id="d4891-279">Para corrigir o problema, tente atualizar o computador.</span><span class="sxs-lookup"><span data-stu-id="d4891-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="d4891-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-282">0x80073D08</span><span class="sxs-lookup"><span data-stu-id="d4891-282">0x80073D08</span></span></td>
<td><span data-ttu-id="d4891-283">Um binário não Windows corrompido foi detectado no sistema.</span><span class="sxs-lookup"><span data-stu-id="d4891-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="d4891-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-286">0x80073D09</span><span class="sxs-lookup"><span data-stu-id="d4891-286">0x80073D09</span></span></td>
<td><span data-ttu-id="d4891-287">A operação não pôde ser retomada porque os dados necessários para a recuperação estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="d4891-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="d4891-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-290">0x80073D0A</span><span class="sxs-lookup"><span data-stu-id="d4891-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="d4891-291">Não foi possível instalar o pacote porque o serviço de firewall do Windows não está em execução.</span><span class="sxs-lookup"><span data-stu-id="d4891-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="d4891-292">Habilite o serviço de firewall do Windows e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="d4891-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="d4891-294">0x80073D0B</span><span class="sxs-lookup"><span data-stu-id="d4891-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="d4891-295">Falha na operação de movimentação de pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="d4891-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-298">0x80073D0C</span><span class="sxs-lookup"><span data-stu-id="d4891-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="d4891-299">A operação de implantação falhou porque o volume não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d4891-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="d4891-301"><strong>OFFLINE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-302">0x80073D0D</span><span class="sxs-lookup"><span data-stu-id="d4891-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="d4891-303">A operação de implantação falhou porque o volume está offline.</span><span class="sxs-lookup"><span data-stu-id="d4891-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="d4891-304">Para uma atualização de pacote, o volume refere-se ao volume instalado de todas as versões de pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="d4891-306"><strong>CORROMPIDO</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-307">0x80073D0E</span><span class="sxs-lookup"><span data-stu-id="d4891-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="d4891-308">A operação de implantação falhou porque o volume especificado está corrompido.</span><span class="sxs-lookup"><span data-stu-id="d4891-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="d4891-310">0x80073D0F</span><span class="sxs-lookup"><span data-stu-id="d4891-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="d4891-311">A operação de implantação falhou porque o aplicativo especificado precisa ser registrado primeiro.</span><span class="sxs-lookup"><span data-stu-id="d4891-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="d4891-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-314">0x80073D10</span><span class="sxs-lookup"><span data-stu-id="d4891-314">0x80073D10</span></span></td>
<td><span data-ttu-id="d4891-315">A operação de implantação falhou porque o pacote se destina à arquitetura de processador incorreta.</span><span class="sxs-lookup"><span data-stu-id="d4891-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="d4891-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-318">0x80073D11</span><span class="sxs-lookup"><span data-stu-id="d4891-318">0x80073D11</span></span></td>
<td><span data-ttu-id="d4891-319">Você atingiu o número máximo de pacotes Sideload do desenvolvedor permitidos neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4891-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="d4891-320">Desinstale um pacote Sideload e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="d4891-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="d4891-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="d4891-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-324">0x80073D12</span><span class="sxs-lookup"><span data-stu-id="d4891-324">0x80073D12</span></span></td>
<td><span data-ttu-id="d4891-325">Um pacote do aplicativo principal é necessário para instalar esse pacote opcional.</span><span class="sxs-lookup"><span data-stu-id="d4891-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="d4891-326">Primeiro, instale o pacote principal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="d4891-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="d4891-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-329">0x80073D13</span><span class="sxs-lookup"><span data-stu-id="d4891-329">0x80073D13</span></span></td>
<td><span data-ttu-id="d4891-330">Este tipo de pacote de aplicativo não tem suporte neste sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d4891-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="d4891-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-333">0x80073D14</span><span class="sxs-lookup"><span data-stu-id="d4891-333">0x80073D14</span></span></td>
<td><span data-ttu-id="d4891-334">A operação de movimentação de pacote é bloqueada até que o aplicativo tenha terminado o streaming.</span><span class="sxs-lookup"><span data-stu-id="d4891-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="d4891-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="d4891-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-338">0x80073D15</span><span class="sxs-lookup"><span data-stu-id="d4891-338">0x80073D15</span></span></td>
<td><span data-ttu-id="d4891-339">Um pacote de aplicativo principal ou outro opcional tem a mesma ID de aplicativo que o pacote opcional.</span><span class="sxs-lookup"><span data-stu-id="d4891-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="d4891-340">Altere a ID do aplicativo para o pacote opcional para evitar conflitos.</span><span class="sxs-lookup"><span data-stu-id="d4891-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="d4891-342"><strong>ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-343">0x80073D16</span><span class="sxs-lookup"><span data-stu-id="d4891-343">0x80073D16</span></span></td>
<td><span data-ttu-id="d4891-344">Esta sessão de preparo foi mantida para permitir que outra operação de preparo seja priorizada.</span><span class="sxs-lookup"><span data-stu-id="d4891-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-347">0x80073D17</span><span class="sxs-lookup"><span data-stu-id="d4891-347">0x80073D17</span></span></td>
<td><span data-ttu-id="d4891-348">Um conjunto relacionado não pode ser atualizado porque o conjunto atualizado é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="d4891-349">Todos os pacotes no conjunto relacionado devem ser atualizados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d4891-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="d4891-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="d4891-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-353">0x80073D18</span><span class="sxs-lookup"><span data-stu-id="d4891-353">0x80073D18</span></span></td>
<td><span data-ttu-id="d4891-354">Um pacote opcional com um ponto de entrada FullTrust exige que o pacote principal tenha o recurso <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="d4891-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-357">0x80073D19</span><span class="sxs-lookup"><span data-stu-id="d4891-357">0x80073D19</span></span></td>
<td><span data-ttu-id="d4891-358">Ocorreu um erro porque um usuário foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="d4891-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="d4891-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="d4891-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-362">0x80073D1A</span><span class="sxs-lookup"><span data-stu-id="d4891-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="d4891-363">Um provisionamento de pacote opcional requer que o pacote principal de dependência também seja provisionado.</span><span class="sxs-lookup"><span data-stu-id="d4891-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="d4891-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-366">0x80073D1B</span><span class="sxs-lookup"><span data-stu-id="d4891-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="d4891-367">Os pacotes falharam na <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">verificação de reputação do SmartScreen</a>.</span><span class="sxs-lookup"><span data-stu-id="d4891-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="d4891-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-370">0x80073D1C</span><span class="sxs-lookup"><span data-stu-id="d4891-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="d4891-371">A operação de <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">verificação de reputação do SmartScreen</a> atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="d4891-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="d4891-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-374">0x80073D1D</span><span class="sxs-lookup"><span data-stu-id="d4891-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="d4891-375">Não há suporte para a opção de implantação atual.</span><span class="sxs-lookup"><span data-stu-id="d4891-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="d4891-377"><strong>ACTIVATION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-378">0x80073D1E</span><span class="sxs-lookup"><span data-stu-id="d4891-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="d4891-379">A ativação está bloqueada devido às configurações de atualização. AppInstaller para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4891-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="d4891-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-382">0x80073D1F</span><span class="sxs-lookup"><span data-stu-id="d4891-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="d4891-383">Não há suporte para unidades remotas.</span><span class="sxs-lookup"><span data-stu-id="d4891-383">Remote drives are not supported.</span></span> <span data-ttu-id="d4891-384">Use <strong> \\ server\share</strong> para registrar um pacote remoto.</span><span class="sxs-lookup"><span data-stu-id="d4891-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="d4891-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-387">0x80073D20</span><span class="sxs-lookup"><span data-stu-id="d4891-387">0x80073D20</span></span></td>
<td><span data-ttu-id="d4891-388">Falha ao processar e gravar os dados de pacote baixados no disco.</span><span class="sxs-lookup"><span data-stu-id="d4891-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="d4891-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-391">0x80073D21</span><span class="sxs-lookup"><span data-stu-id="d4891-391">0x80073D21</span></span></td>
<td><span data-ttu-id="d4891-392">A operação de implantação foi bloqueada devido a uma política da família por pacote restringindo implantações em um volume que não é do sistema.</span><span class="sxs-lookup"><span data-stu-id="d4891-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="d4891-393">Por política, esse aplicativo deve ser instalado na unidade do sistema, mas não é definido como o padrão.</span><span class="sxs-lookup"><span data-stu-id="d4891-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="d4891-394">Em configurações de armazenamento, torne a unidade do sistema o local padrão para salvar o novo conteúdo e repita a instalação.</span><span class="sxs-lookup"><span data-stu-id="d4891-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="d4891-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-397">0x80073D22</span><span class="sxs-lookup"><span data-stu-id="d4891-397">0x80073D22</span></span></td>
<td><span data-ttu-id="d4891-398">A operação de implantação foi bloqueada devido a uma política de todo o computador restringindo implantações em um volume que não é do sistema.</span><span class="sxs-lookup"><span data-stu-id="d4891-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="d4891-399">Por política, esse aplicativo deve ser instalado na unidade do sistema, mas não é definido como o padrão.</span><span class="sxs-lookup"><span data-stu-id="d4891-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="d4891-400">Em configurações de armazenamento, torne a unidade do sistema o local padrão para salvar o novo conteúdo e repita a instalação.</span><span class="sxs-lookup"><span data-stu-id="d4891-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="d4891-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-403">0x80073D23</span><span class="sxs-lookup"><span data-stu-id="d4891-403">0x80073D23</span></span></td>
<td><span data-ttu-id="d4891-404">A operação de implantação foi bloqueada porque a implantação de perfil especial não é permitida (perfis especiais são perfis de usuário em que as alterações são descartadas após o usuário sair).</span><span class="sxs-lookup"><span data-stu-id="d4891-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="d4891-405">Tente fazer logon em uma conta que não seja um perfil especial.</span><span class="sxs-lookup"><span data-stu-id="d4891-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="d4891-406">Você pode tentar fazer logoff e logon novamente na conta atual ou tentar fazer logon em uma conta diferente.</span><span class="sxs-lookup"><span data-stu-id="d4891-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="d4891-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-409"><strong>ACTIVE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-410">0x80073D24</span><span class="sxs-lookup"><span data-stu-id="d4891-410">0x80073D24</span></span></td>
<td><span data-ttu-id="d4891-411">A operação de implantação falhou devido a um <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">diretório de pacote mutável</a>do pacote conflitante.</span><span class="sxs-lookup"><span data-stu-id="d4891-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="d4891-412">Para instalar este pacote, remova o pacote existente com o diretório de pacote mutável conflitante.</span><span class="sxs-lookup"><span data-stu-id="d4891-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="d4891-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-415">0x80073D25</span><span class="sxs-lookup"><span data-stu-id="d4891-415">0x80073D25</span></span></td>
<td><span data-ttu-id="d4891-416">A instalação do pacote falhou porque um recurso singleton foi especificado e outro usuário com esse pacote instalado está conectado.</span><span class="sxs-lookup"><span data-stu-id="d4891-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="d4891-417">Verifique se todos os usuários ativos com o pacote instalado estão desconectados e tente novamente a instalação.</span><span class="sxs-lookup"><span data-stu-id="d4891-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="d4891-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="d4891-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-420">0x80073D26</span><span class="sxs-lookup"><span data-stu-id="d4891-420">0x80073D26</span></span></td>
<td><span data-ttu-id="d4891-421">A instalação do pacote falhou porque uma versão diferente do serviço está instalada.</span><span class="sxs-lookup"><span data-stu-id="d4891-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="d4891-422">Tente instalar uma versão mais recente do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="d4891-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-425">0x80073D27</span><span class="sxs-lookup"><span data-stu-id="d4891-425">0x80073D27</span></span></td>
<td><span data-ttu-id="d4891-426">A instalação do pacote falhou porque existe uma versão do serviço fora de um pacote. msix/. Appx.</span><span class="sxs-lookup"><span data-stu-id="d4891-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="d4891-427">Contate o fornecedor do software.</span><span class="sxs-lookup"><span data-stu-id="d4891-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="d4891-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-430">0x80073D28</span><span class="sxs-lookup"><span data-stu-id="d4891-430">0x80073D28</span></span></td>
<td><span data-ttu-id="d4891-431">A instalação do pacote falhou porque são necessários privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="d4891-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="d4891-432">Contate um administrador para instalar este pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="d4891-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-435">0x80073D29</span><span class="sxs-lookup"><span data-stu-id="d4891-435">0x80073D29</span></span></td>
<td><span data-ttu-id="d4891-436">A implantação do pacote falhou porque a operação seria redirecionada para a conta padrão, quando o chamador disse que não fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d4891-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="d4891-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-439">0x80073D2A</span><span class="sxs-lookup"><span data-stu-id="d4891-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="d4891-440">A implantação do pacote falhou porque o pacote requer um recurso para direcionar nativamente esse host.</span><span class="sxs-lookup"><span data-stu-id="d4891-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-443">0x80073D2B</span><span class="sxs-lookup"><span data-stu-id="d4891-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="d4891-444">A implantação do pacote falhou porque seu conteúdo não é válido para um pacote não assinado.</span><span class="sxs-lookup"><span data-stu-id="d4891-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-447">0x80073D2C</span><span class="sxs-lookup"><span data-stu-id="d4891-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="d4891-448">A implantação do pacote falhou porque seu Publicador não está no namespace não assinado.</span><span class="sxs-lookup"><span data-stu-id="d4891-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-451">0x80073D2D</span><span class="sxs-lookup"><span data-stu-id="d4891-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="d4891-452">A implantação do pacote falhou porque seu Publicador não está no namespace assinado.</span><span class="sxs-lookup"><span data-stu-id="d4891-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="d4891-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-455">0x80073D2E</span><span class="sxs-lookup"><span data-stu-id="d4891-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="d4891-456">A implantação do pacote falhou porque seu Publicador não está no namespace assinado.</span><span class="sxs-lookup"><span data-stu-id="d4891-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="d4891-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="d4891-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-460">0x80073D2F</span><span class="sxs-lookup"><span data-stu-id="d4891-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="d4891-461">Uma dependência de tempo de execução de host resolvendo para um pacote com conteúdo de confiança total requer que o pacote principal tenha o recurso <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4891-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="d4891-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="d4891-463">0x80080200</span></span></td>
<td><span data-ttu-id="d4891-464">A API de empacotamento encontrou um erro interno.</span><span class="sxs-lookup"><span data-stu-id="d4891-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="d4891-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="d4891-467">0x80080201</span></span></td>
<td><span data-ttu-id="d4891-468">O pacote não é válido porque seu conteúdo é intercalado.</span><span class="sxs-lookup"><span data-stu-id="d4891-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="d4891-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="d4891-471">0x80080202</span></span></td>
<td><span data-ttu-id="d4891-472">O pacote não é válido porque contém relações OPC.</span><span class="sxs-lookup"><span data-stu-id="d4891-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="d4891-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="d4891-475">0x80080203</span></span></td>
<td><span data-ttu-id="d4891-476">O pacote não é válido porque está faltando um manifesto ou um mapa de bloco ou um arquivo de integridade de código está presente, mas um arquivo de assinatura está ausente.</span><span class="sxs-lookup"><span data-stu-id="d4891-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="d4891-477">Verifique se o pacote não tem um ou mais desses arquivos necessários:</span><span class="sxs-lookup"><span data-stu-id="d4891-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="d4891-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="d4891-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="d4891-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="d4891-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="d4891-480">Se o pacote contiver \AppxMetadata\CodeIntegrity.cat, ele também deverá conter \AppxSignature.p7x.</span><span class="sxs-lookup"><span data-stu-id="d4891-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="d4891-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="d4891-482">0x80080204</span></span></td>
<td><span data-ttu-id="d4891-483">O arquivo de AppxManifest.xml do pacote não é válido.</span><span class="sxs-lookup"><span data-stu-id="d4891-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="d4891-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="d4891-485">0x80080205</span></span></td>
<td><span data-ttu-id="d4891-486">O arquivo de AppxBlockMap.xml do pacote não é válido.</span><span class="sxs-lookup"><span data-stu-id="d4891-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="d4891-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="d4891-488">0x80080206</span></span></td>
<td><span data-ttu-id="d4891-489">O conteúdo do pacote não pode ser lido porque está corrompido.</span><span class="sxs-lookup"><span data-stu-id="d4891-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="d4891-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="d4891-492">0x80080207</span></span></td>
<td><span data-ttu-id="d4891-493">O valor de hash calculado do bloco não corresponde ao valor de tem armazenado no mapa de bloco.</span><span class="sxs-lookup"><span data-stu-id="d4891-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="d4891-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="d4891-496">0x80080208</span></span></td>
<td><span data-ttu-id="d4891-497">O intervalo de bytes solicitado é de mais de 4 GB quando convertido em um intervalo de bytes de blocos.</span><span class="sxs-lookup"><span data-stu-id="d4891-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="d4891-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="d4891-499">0x800B0100</span></span></td>
<td><span data-ttu-id="d4891-500">Nenhuma assinatura está presente no assunto.</span><span class="sxs-lookup"><span data-stu-id="d4891-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="d4891-501">Você poderá receber esse erro se o pacote não estiver assinado ou se a assinatura não for válida.</span><span class="sxs-lookup"><span data-stu-id="d4891-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="d4891-502">O pacote deve ser assinado para ser implantado.</span><span class="sxs-lookup"><span data-stu-id="d4891-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="d4891-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="d4891-504">0x800B0109</span></span></td>
<td><span data-ttu-id="d4891-505">Uma cadeia de certificados foi processada, mas terminada em um certificado raiz que não é confiável pelo provedor de confiança.</span><span class="sxs-lookup"><span data-stu-id="d4891-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="d4891-506">Consulte <a href="/previous-versions/br230260(v=vs.110)">assinando um pacote</a>.</span><span class="sxs-lookup"><span data-stu-id="d4891-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="d4891-508">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="d4891-508">0x800B010A</span></span></td>
<td><span data-ttu-id="d4891-509">Não foi possível criar uma cadeia de certificados para uma autoridade de certificação raiz confiável.</span><span class="sxs-lookup"><span data-stu-id="d4891-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="d4891-510">Consulte <a href="/previous-versions/br230260(v=vs.110)">assinando um pacote</a>.</span><span class="sxs-lookup"><span data-stu-id="d4891-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="d4891-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="d4891-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="d4891-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="d4891-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="d4891-513">0x80080209</span></span></td>
<td><span data-ttu-id="d4891-514">A estrutura de <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>usada para assinar o pacote não contém os dados necessários</span><span class="sxs-lookup"><span data-stu-id="d4891-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="d4891-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="d4891-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="d4891-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="d4891-517">0x8008020A</span><span class="sxs-lookup"><span data-stu-id="d4891-517">0x8008020A</span></span></td>
<td><span data-ttu-id="d4891-518">A estrutura de <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> usada para criptografar ou descriptografar o pacote contém dados inválidos.</span><span class="sxs-lookup"><span data-stu-id="d4891-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-520"><strong>CONTENTGROUPMAP</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-521">0x8008020B</span><span class="sxs-lookup"><span data-stu-id="d4891-521">0x8008020B</span></span></td>
<td><span data-ttu-id="d4891-522">O mapa do grupo de conteúdo do pacote. msix/. Appx é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-524"><strong>APPINSTALLER</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-525">0x8008020C</span><span class="sxs-lookup"><span data-stu-id="d4891-525">0x8008020C</span></span></td>
<td><span data-ttu-id="d4891-526">O <a href="/windows/msix/app-installer/app-installer-root">arquivo. AppInstaller</a> do pacote é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="d4891-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-529">0x8008020D</span><span class="sxs-lookup"><span data-stu-id="d4891-529">0x8008020D</span></span></td>
<td><span data-ttu-id="d4891-530">A versão do pacote de linha de base no pacote Delta não corresponde à versão do pacote de linha de base a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d4891-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="d4891-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-533">0x8008020E</span><span class="sxs-lookup"><span data-stu-id="d4891-533">0x8008020E</span></span></td>
<td><span data-ttu-id="d4891-534">O pacote Delta não tem um arquivo do pacote atualizado.</span><span class="sxs-lookup"><span data-stu-id="d4891-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-537">0x8008020F</span><span class="sxs-lookup"><span data-stu-id="d4891-537">0x8008020F</span></span></td>
<td><span data-ttu-id="d4891-538">O pacote delta é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="d4891-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="d4891-541">0x80080210</span></span></td>
<td><span data-ttu-id="d4891-542">O pacote Delta anexado não é permitido para a operação atual.</span><span class="sxs-lookup"><span data-stu-id="d4891-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="d4891-545">0x80080211</span></span></td>
<td><span data-ttu-id="d4891-546">O arquivo de layout de empacotamento é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-548"><strong>PACKAGESIGNCONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="d4891-549">0x80080212</span></span></td>
<td><span data-ttu-id="d4891-550">O arquivo packageSignConfig é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="d4891-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="d4891-553">0x80080213</span></span></td>
<td><span data-ttu-id="d4891-554">O arquivo Resources. pri não é permitido quando não há elementos de recurso no manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4891-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="d4891-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="d4891-557">0x80080214</span></span></td>
<td><span data-ttu-id="d4891-558">O estado de compactação do arquivo na linha de base e no pacote atualizado não corresponde.</span><span class="sxs-lookup"><span data-stu-id="d4891-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4891-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="d4891-561">0x80080215</span></span></td>
<td><span data-ttu-id="d4891-562">Extensões não. Appx não são permitidas para pacotes de carga destinados a plataformas mais antigas.</span><span class="sxs-lookup"><span data-stu-id="d4891-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4891-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="d4891-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="d4891-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="d4891-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="d4891-565">0x80080216</span></span></td>
<td><span data-ttu-id="d4891-566">O arquivo encryptionExclusionFileList é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4891-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="d4891-567">Os aplicativos não são iniciados e seus nomes ficam esmaecidos</span><span class="sxs-lookup"><span data-stu-id="d4891-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="d4891-568">Em um computador baseado no Windows 10, você não pode iniciar alguns aplicativos e os nomes dos aplicativos aparecem esmaecidos.</span><span class="sxs-lookup"><span data-stu-id="d4891-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![Alguns nomes de aplicativos aparecem esmaecidos no menu iniciar](./images/app-names-dimmed.png)

<span data-ttu-id="d4891-570">Ao tentar abrir um aplicativo selecionando o nome esmaecido, você poderá receber uma das seguintes mensagens de erro:</span><span class="sxs-lookup"><span data-stu-id="d4891-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="d4891-571">Há um problema com o \<*application name*> .</span><span class="sxs-lookup"><span data-stu-id="d4891-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="d4891-572">Contate o administrador do sistema para reparar ou reinstalá-lo</span><span class="sxs-lookup"><span data-stu-id="d4891-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="d4891-573">Erro: este aplicativo não pode ser aberto</span><span class="sxs-lookup"><span data-stu-id="d4891-573">Error: This app can't open</span></span>

<span data-ttu-id="d4891-574">Além disso, as entradas de evento a seguir são registradas no log "Microsoft-Windows-TWinUI/Operational" em **Applications and Services\Microsoft\Windows\Apps**:</span><span class="sxs-lookup"><span data-stu-id="d4891-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="d4891-575">Nome do log: Microsoft-Windows-TWinUI/Operational</span><span class="sxs-lookup"><span data-stu-id="d4891-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="d4891-576">Fonte: Microsoft-Windows-imersiva-Shell</span><span class="sxs-lookup"><span data-stu-id="d4891-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="d4891-577">Data: *Data* de <></span><span class="sxs-lookup"><span data-stu-id="d4891-577">Date: <*date*></span></span>  
> <span data-ttu-id="d4891-578">ID do evento: 5960</span><span class="sxs-lookup"><span data-stu-id="d4891-578">Event ID: 5960</span></span>  
> <span data-ttu-id="d4891-579">Categoria da tarefa: (5960)</span><span class="sxs-lookup"><span data-stu-id="d4891-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="d4891-580">Nível: erro</span><span class="sxs-lookup"><span data-stu-id="d4891-580">Level: Error</span></span>  
> <span data-ttu-id="d4891-581">Palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="d4891-581">Keywords:</span></span>  
> <span data-ttu-id="d4891-582">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4891-582">Description:</span></span>  
> <span data-ttu-id="d4891-583">Ativação do aplicativo Microsoft.BingNews_8wekyb3d8bbwe! AppexNews para o Windows.</span><span class="sxs-lookup"><span data-stu-id="d4891-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="d4891-584">O contrato de inicialização foi bloqueado com o erro 0x80073CFC porque seu pacote está em estado: modificado.</span><span class="sxs-lookup"><span data-stu-id="d4891-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="d4891-585">Causa</span><span class="sxs-lookup"><span data-stu-id="d4891-585">Cause</span></span>

<span data-ttu-id="d4891-586">Esse problema ocorre porque a entrada do registro para o valor de status do pacote correspondente do aplicativo foi modificada.</span><span class="sxs-lookup"><span data-stu-id="d4891-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="d4891-587">Resolução</span><span class="sxs-lookup"><span data-stu-id="d4891-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="d4891-588">Podem ocorrer problemas sérios se você modificar o Registro incorretamente, usando o Editor do Registro ou outro método.</span><span class="sxs-lookup"><span data-stu-id="d4891-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="d4891-589">Esses problemas podem exigir que você reinstale o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d4891-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="d4891-590">A Microsoft não garante que esses problemas possam ser solucionados.</span><span class="sxs-lookup"><span data-stu-id="d4891-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="d4891-591">Modifique o Registro por conta própria.</span><span class="sxs-lookup"><span data-stu-id="d4891-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="d4891-592">Para corrigir esse problema:</span><span class="sxs-lookup"><span data-stu-id="d4891-592">To fix this issue:</span></span>

1. <span data-ttu-id="d4891-593">Inicie o editor do registro e localize a subchave **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .</span><span class="sxs-lookup"><span data-stu-id="d4891-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="d4891-594">Para fazer backup dos dados da subchave, clique com o botão direito do mouse em **PackageList**, selecione **Exportar** e, em seguida, salve os dados como um arquivo do registro.</span><span class="sxs-lookup"><span data-stu-id="d4891-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="d4891-595">Para cada um dos aplicativos listados nas entradas de log da ID de evento 5960, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4891-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="d4891-596">Localize a entrada **PackageStatus** .</span><span class="sxs-lookup"><span data-stu-id="d4891-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="d4891-597">Defina o valor de **PackageStatus** como zero (**0**).</span><span class="sxs-lookup"><span data-stu-id="d4891-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="d4891-598">Se não houver entradas para o aplicativo em **PackageList**, o problema terá alguma outra causa.</span><span class="sxs-lookup"><span data-stu-id="d4891-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="d4891-599">No caso do evento de exemplo neste artigo, a subchave completa é **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="d4891-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="d4891-600">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="d4891-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="d4891-601">Obter ajuda técnica</span><span class="sxs-lookup"><span data-stu-id="d4891-601">Get additional help</span></span>

<span data-ttu-id="d4891-602">Se precisar de ajuda adicional para resolver um problema que você está experimentando ao empacotar, implantar ou consultar um pacote de aplicativo do Windows (. msix/. AppX) como desenvolvedor, consulte esses recursos adicionais de suporte do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="d4891-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="d4891-603">O [Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) oferece respostas relevantes e oportunas aos problemas técnicos de uma comunidade de especialistas e engenheiros da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d4891-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="d4891-604">Para assistência da Comunidade com perguntas de desenvolvimento, há nossos [fóruns](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)e [StackOverflow](https://stackoverflow.com/questions).</span><span class="sxs-lookup"><span data-stu-id="d4891-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="d4891-605">O site de [suporte do desenvolvedor do Windows](https://developer.microsoft.com/windows/support) explica outras opções de suporte.</span><span class="sxs-lookup"><span data-stu-id="d4891-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4891-606">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4891-606">Related topics</span></span>

- [<span data-ttu-id="d4891-607">Como assinar um pacote de aplicativos usando o SignTool</span><span class="sxs-lookup"><span data-stu-id="d4891-607">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
- [<span data-ttu-id="d4891-608">Como solucionar problemas de erros de assinatura do pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d4891-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)
