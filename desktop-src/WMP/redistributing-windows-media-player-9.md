---
title: Redistribuindo o Windows Media Player 9 Series
description: Redistribuindo o Windows Media Player 9 Series
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006061"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="08e28-103">Redistribuindo o Windows Media Player 9 Series</span><span class="sxs-lookup"><span data-stu-id="08e28-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="08e28-104">Você pode instalar o Windows Media Player 9 Series no Windows XP usando um dos programas de instalação a seguir.</span><span class="sxs-lookup"><span data-stu-id="08e28-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="08e28-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="08e28-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="08e28-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="08e28-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="08e28-107">MPSetup.exe é um superconjunto do programa de instalação do MPSetupXP.exe.</span><span class="sxs-lookup"><span data-stu-id="08e28-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="08e28-108">Ele contém arquivos que são necessários para sistemas operacionais lançados antes do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08e28-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="08e28-109">MPSetup.exe é funcionalmente equivalente a MPSetupXP.exe quando executado no Windows XP, mas o tamanho do arquivo do programa de instalação é maior porque não foi otimizado para instalação em sistemas operacionais Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08e28-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="08e28-110">Você pode instalar o Windows Media Player 9 Series no Windows 98 Second Edition, no Windows Millennium Edition ou no Windows 2000 usando o seguinte programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="08e28-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="08e28-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="08e28-111">MPSetup.exe</span></span>

<span data-ttu-id="08e28-112">Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e nenhum prompt de reinicialização ou reinicialização.</span><span class="sxs-lookup"><span data-stu-id="08e28-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="08e28-113">O parâmetro/P: \# e especifica que o pacote de instalação do Windows Media Player deve ser armazenado em cache durante a instalação do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="08e28-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="08e28-114">Esse comando é usado para lidar com atualizações futuras do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08e28-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="08e28-115">Esse comando deve ser omitido somente por administradores de ti corporativos.</span><span class="sxs-lookup"><span data-stu-id="08e28-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="08e28-116">O único caso em que/P: \# e não deve ser incluído na linha de comando é quando você possui o sistema de destino e sabe que o sistema de destino nunca será atualizado para um sistema operacional posterior.</span><span class="sxs-lookup"><span data-stu-id="08e28-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="08e28-117">Por exemplo, se você estiver instalando o Windows Media Player 9 Series no Windows 2000 e o computador puder ser atualizado para o Windows XP, você deverá usar/P: \# e na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="08e28-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="08e28-118">Caso contrário, após a instalação do Windows XP, os arquivos do Windows Media Player serão substituídos pelos arquivos do Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08e28-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="08e28-119">A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação do Windows Media Player 9 Series.</span><span class="sxs-lookup"><span data-stu-id="08e28-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="08e28-120">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="08e28-120">Parameter</span></span>              | <span data-ttu-id="08e28-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="08e28-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e28-122">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="08e28-122">/NoMigrate</span></span>             | <span data-ttu-id="08e28-123">Impedir a migração da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="08e28-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="08e28-124">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="08e28-124">/NestedRestore</span></span>         | <span data-ttu-id="08e28-125">Crie um ponto de restauração do sistema aninhado.</span><span class="sxs-lookup"><span data-stu-id="08e28-125">Create a nested system restore point.</span></span> <span data-ttu-id="08e28-126">Use esta se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto de restauração do Windows Media Player no ponto de restauração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08e28-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="08e28-127">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="08e28-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="08e28-128">Não permitir a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="08e28-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="08e28-129">Esse sinalizador desabilitará a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="08e28-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="08e28-130">Na maioria das circunstâncias, esse sinalizador não deve ser usado para a redistribuição de software geral.</span><span class="sxs-lookup"><span data-stu-id="08e28-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="08e28-131">Isso deve ser usado somente quando você pode fazer uma escolha explícita em nome do usuário final para não oferecer suporte à reversão dos arquivos do Windows Media Player para uma versão anterior do Player.</span><span class="sxs-lookup"><span data-stu-id="08e28-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="08e28-132">Esse sinalizador deve ser usado somente para a implantação corporativa ou para a instalação do OEM (fabricante original do equipamento).</span><span class="sxs-lookup"><span data-stu-id="08e28-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="08e28-133">Observações</span><span class="sxs-lookup"><span data-stu-id="08e28-133">Notes</span></span>

-   <span data-ttu-id="08e28-134">Os parâmetros de linha de comando diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="08e28-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="08e28-135">Ao suprimir o prompt de reinicialização, você deve verificar a chave do registro InstallResult e tratar a notificação de reinicialização no aplicativo de instalação de chamada.</span><span class="sxs-lookup"><span data-stu-id="08e28-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="08e28-136">O Windows Media Player 9 Series também instala o tempo de execução do Windows Media Format, portanto, não é necessário incluir o pacote de distribuição do Windows Media Player e o pacote de distribuição do Windows Media Format no mesmo pacote de redistribuição de software.</span><span class="sxs-lookup"><span data-stu-id="08e28-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="08e28-137">Portanto, se você incluir MPSetup.exe ou MPSetupXP.exe em sua instalação, não será necessário incluir WMFdist.exe.</span><span class="sxs-lookup"><span data-stu-id="08e28-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e28-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08e28-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e28-139">**Redistribuindo o software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="08e28-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




