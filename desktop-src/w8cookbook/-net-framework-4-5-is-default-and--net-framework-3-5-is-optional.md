---
title: .NET Framework configurações padrão
description: .NET Framework 4,5 é o padrão e .NET Framework 3,5 é opcional
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "105784670"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="0f94e-103">.NET Framework 4,5 é o padrão e .NET Framework 3,5 é opcional</span><span class="sxs-lookup"><span data-stu-id="0f94e-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="0f94e-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="0f94e-104">Platforms</span></span>

<span data-ttu-id="0f94e-105">**Clientes**   do   Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f94e-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="0f94e-106">**Servidores**   do   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f94e-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="0f94e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f94e-107">Description</span></span>

<span data-ttu-id="0f94e-108">O .NET Framework 4,5 está habilitado por padrão no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0f94e-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="0f94e-109">O Windows 8 não inclui o .NET 3,5 por padrão, mas os arquivos para o .NET 3,5 estão disponíveis na mídia de instalação do Windows 8 como um recurso opcional.</span><span class="sxs-lookup"><span data-stu-id="0f94e-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="0f94e-110">Se o usuário estiver atualizando do Windows 7 para o Windows 8, .NET Framework 3,5 será totalmente habilitado para garantir que todos os aplicativos no computador continuem a funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="0f94e-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0f94e-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="0f94e-111">Manifestation</span></span>

<span data-ttu-id="0f94e-112">Se o usuário executar uma instalação limpa do Windows 8 e, em seguida, instalar aplicativos que exigem o .NET Framework 3,5 (ou 2,0), eles dispararão uma solicitação para os arquivos do .NET 3,5 necessários.</span><span class="sxs-lookup"><span data-stu-id="0f94e-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="0f94e-113">Normalmente, os arquivos ausentes serão baixados de Windows Update (depois de solicitar a permissão ao usuário), mas se o acesso ao Windows Update não for possível, a habilitação .NET Framework 3,5 falhará, a menos que uma fonte alternativa para os arquivos ausentes tenha sido especificada.</span><span class="sxs-lookup"><span data-stu-id="0f94e-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="0f94e-114">Atenuação</span><span class="sxs-lookup"><span data-stu-id="0f94e-114">Mitigation</span></span>

<span data-ttu-id="0f94e-115">Para habilitar o .NET Framework 3,5 somente em máquinas de teste com instalações limpas do Windows 8:</span><span class="sxs-lookup"><span data-stu-id="0f94e-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="0f94e-116">Copie \\ \\ as fontes SxS \\ da imagem ISO Build do sistema operacional montado para dotnet35 ou para uma pasta semelhante.</span><span class="sxs-lookup"><span data-stu-id="0f94e-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="0f94e-117">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0f94e-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="0f94e-118">Execute esta linha de comando usando privilégios de administrador:</span><span class="sxs-lookup"><span data-stu-id="0f94e-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="0f94e-119">A \\ pasta SxS de fontes não deve ser usada como um mecanismo de redistribuição, pois não é um mecanismo com suporte.</span><span class="sxs-lookup"><span data-stu-id="0f94e-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="0f94e-120">Solução</span><span class="sxs-lookup"><span data-stu-id="0f94e-120">Solution</span></span>

<span data-ttu-id="0f94e-121">**Para consumidores:**</span><span class="sxs-lookup"><span data-stu-id="0f94e-121">**For consumers:**</span></span>

<span data-ttu-id="0f94e-122">O Windows 8 inclui um mecanismo que habilita automaticamente .NET Framework 3,5 ao tentar instalar o pacote redistribuível ou quando um instalador de aplicativo que precisa do .NET 3,5 invoca o redistribuível.</span><span class="sxs-lookup"><span data-stu-id="0f94e-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="0f94e-123">**Para desenvolvedores de aplicativos (e administradores de ti):**</span><span class="sxs-lookup"><span data-stu-id="0f94e-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="0f94e-124">Os administradores de ti podem configurar aplicativos .NET 3,5 para serem executados no .NET 3,5 ou no .NET 4,5 (dependendo do que já está instalado).</span><span class="sxs-lookup"><span data-stu-id="0f94e-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="0f94e-125">Para executar um aplicativo gerenciado em 3,5 ou 4,5, basta adicionar uma seção no arquivo de configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f94e-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="0f94e-126">Isso garantirá que, se o .NET 3,5 estiver instalado, o aplicativo será executado no .NET 3,5; caso contrário, o aplicativo será executado no .NET 4,5.</span><span class="sxs-lookup"><span data-stu-id="0f94e-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="0f94e-127">Um exemplo da seção adicional no arquivo de configuração é fornecido abaixo:</span><span class="sxs-lookup"><span data-stu-id="0f94e-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="0f94e-128">**Para OEMs corporativos:**</span><span class="sxs-lookup"><span data-stu-id="0f94e-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="0f94e-129">Para habilitar o .NET Framework 3,5 para compilações do EEAP e para aplicativos que não têm acesso ao Windows Update:</span><span class="sxs-lookup"><span data-stu-id="0f94e-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="0f94e-130">Copie \\ o \\ SxS \\ de fontes da imagem ISO de Build do sistema operacional montado para o dotnet35 ou para a pasta semelhante.</span><span class="sxs-lookup"><span data-stu-id="0f94e-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="0f94e-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0f94e-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="0f94e-132">Defina o RegKey:</span><span class="sxs-lookup"><span data-stu-id="0f94e-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="0f94e-133">**Para empresas:**</span><span class="sxs-lookup"><span data-stu-id="0f94e-133">**For enterprises:**</span></span>

<span data-ttu-id="0f94e-134">Para computadores configurados para usar o WSUS para manutenção, você pode definir uma entrada de registro para permitir que o computador Use Windows Update para habilitar o .NET 3,5 em vez do WSUS (a manutenção ainda será feita do WSUS se você fizer isso).</span><span class="sxs-lookup"><span data-stu-id="0f94e-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="0f94e-135">Defina o RegKey:</span><span class="sxs-lookup"><span data-stu-id="0f94e-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="0f94e-136">Essa entrada de registro também pode ser definida por meio de Política de Grupo (política de computador local-> configuração do computador-> sistema Modelos Administrativos->.</span><span class="sxs-lookup"><span data-stu-id="0f94e-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="0f94e-137">Selecione a configuração especificar configurações para instalação de componente opcional e reparo de componentes.</span><span class="sxs-lookup"><span data-stu-id="0f94e-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="0f94e-138">Se você selecionar contatar Windows Update diretamente para baixar conteúdo de reparo em vez de Windows Server Update Services (WSUS), quaisquer tentativas de adicionar recursos do Windows (por exemplo, .NET Framework 3,5) ou reparar recursos irão disparar downloads de arquivo do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="0f94e-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="0f94e-139">Os computadores de destino exigem acesso de Internet e WU para essa opção.</span><span class="sxs-lookup"><span data-stu-id="0f94e-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="0f94e-140">As operações normais de manutenção continuam a usar o WSUS se ele tiver sido configurado como uma origem.</span><span class="sxs-lookup"><span data-stu-id="0f94e-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="0f94e-141">**Uma observação sobre como definir o local de origem local por meio de entradas do registro**</span><span class="sxs-lookup"><span data-stu-id="0f94e-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="0f94e-142">Os administradores de ti podem definir locais de origem local para arquivos .NET 3,5 por meio de uma entrada de registro, para que os usuários possam usar a caixa de diálogo Adicionar/remover recursos do Windows para habilitar recursos com carga ausente sem precisar especificar um local de origem.</span><span class="sxs-lookup"><span data-stu-id="0f94e-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="0f94e-143">O valor da entrada do registro pode ser controlado por meio da diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0f94e-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="0f94e-144">Há suporte para essa entrada de registro:</span><span class="sxs-lookup"><span data-stu-id="0f94e-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0f94e-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f94e-145">Entry</span></span></th>
<th><span data-ttu-id="0f94e-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f94e-146">Type</span></span></th>
<th><span data-ttu-id="0f94e-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f94e-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f94e-148">Caminho de origem local</span><span class="sxs-lookup"><span data-stu-id="0f94e-148">Local Source Path</span></span></td>
<td><span data-ttu-id="0f94e-149">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="0f94e-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="0f94e-150">Caminho (s) de origem local a serem usados por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f94e-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="0f94e-151">Vários caminhos podem ser especificados; Eles devem ser separados por;.</span><span class="sxs-lookup"><span data-stu-id="0f94e-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="0f94e-152">Os locais serão pesquisados na ordem em que são especificados.</span><span class="sxs-lookup"><span data-stu-id="0f94e-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="0f94e-153">Locais de origem local que são especificados na linha de comando do DISM, têm precedência sobre os locais especificados nessa entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="0f94e-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="0f94e-154">Os locais de pasta podem ser especificados nessa entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="0f94e-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="0f94e-155">WIMs pode ser usado, mas o caminho deve ser para o arquivo WIM; Não é necessário montá-lo, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0f94e-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="0f94e-156">Wim: \\ machine\share\file.wim: 1</span><span class="sxs-lookup"><span data-stu-id="0f94e-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="0f94e-157">Observe o 1 no final.</span><span class="sxs-lookup"><span data-stu-id="0f94e-157">Notice the  1  at the end.</span></span> <span data-ttu-id="0f94e-158">Você deve especificar o índice numérico da imagem que deseja usar no arquivo WIM.</span><span class="sxs-lookup"><span data-stu-id="0f94e-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="0f94e-159">Para um WIM montado, o caminho de origem precisa se referir ao diretório do Windows da imagem montada, e não ao ponto de montagem (por exemplo:/Source: <mount_point> \Windows em vez de/Source: <mount_point> ).</span><span class="sxs-lookup"><span data-stu-id="0f94e-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="0f94e-160">Recursos</span><span class="sxs-lookup"><span data-stu-id="0f94e-160">Resources</span></span>

<dl>

[<span data-ttu-id="0f94e-161">Implementando a política baseada no registro</span><span class="sxs-lookup"><span data-stu-id="0f94e-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>