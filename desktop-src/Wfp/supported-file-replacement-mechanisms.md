---
description: Há suporte para a substituição de recursos protegidos por meio dos mecanismos a seguir.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mecanismos de substituição de recursos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796146"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="846c7-103">Mecanismos de substituição de recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="846c7-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="846c7-104">Há suporte para a substituição de recursos protegidos por meio dos mecanismos a seguir.</span><span class="sxs-lookup"><span data-stu-id="846c7-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="846c7-105">Permissão para acesso completo para modificar recursos protegidos por WRP no Windows Vista e no Windows Server 2008 é restrita ao TrustedInstaller com o serviço instalador de módulos do Windows usando os seguintes mecanismos:</span><span class="sxs-lookup"><span data-stu-id="846c7-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="846c7-106">Service Packs do Windows instalados pelo TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="846c7-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="846c7-107">Hotfixes instalados pelo TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="846c7-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="846c7-108">Atualizações do sistema operacional instaladas pelo TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="846c7-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="846c7-109">Windows Update instalado pelo TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="846c7-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="846c7-110">Os aplicativos e instaladores tentando substituir um recurso protegido por WRP por meio de outros métodos especificados têm acesso negado para alterar o recurso e gerar uma mensagem de erro de acesso negado.</span><span class="sxs-lookup"><span data-stu-id="846c7-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="846c7-111">Para instaladores conhecidos que tentam substituir recursos protegidos por WRP, o erro de acesso negado e a mensagem de erro podem ser suprimidos.</span><span class="sxs-lookup"><span data-stu-id="846c7-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="846c7-112">Nesse caso, a operação retorna com êxito, o erro e a mensagem de erro são suprimidos, mas nenhuma alteração é aplicada ao recurso protegido por WRP.</span><span class="sxs-lookup"><span data-stu-id="846c7-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="846c7-113">O erro pode ser suprimido para um instalador bem conhecido somente quando todos os critérios a seguir são atendidos:</span><span class="sxs-lookup"><span data-stu-id="846c7-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="846c7-114">Este é um aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="846c7-114">This is a legacy application.</span></span> <span data-ttu-id="846c7-115">O aplicativo não inclui um manifesto com um requestedExecutionlevel que identifica o aplicativo como projetado para o Windows Vista ou o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="846c7-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="846c7-116">O erro de acesso negado é causado apenas pela tentativa de modificar um recurso protegido por WRP.</span><span class="sxs-lookup"><span data-stu-id="846c7-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="846c7-117">Um administrador está instalando o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="846c7-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="846c7-118">Para obter informações sobre como usar o Windows Installer com a WRP, consulte [usando Windows Installer e proteção de recursos do Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) no SDK do [Windows Installer](/windows/desktop/Msi/windows-installer-portal) .</span><span class="sxs-lookup"><span data-stu-id="846c7-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="846c7-119">**Windows Server 2003 e Windows XP:** A substituição de arquivos do sistema protegidos por WFP tem suporte apenas por meio dos seguintes mecanismos:</span><span class="sxs-lookup"><span data-stu-id="846c7-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="846c7-120">Instalação do Service Pack do Windows usando o Update.exe</span><span class="sxs-lookup"><span data-stu-id="846c7-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="846c7-121">Hotfixes instalados usando o Hotfix.exe</span><span class="sxs-lookup"><span data-stu-id="846c7-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="846c7-122">Atualizações do sistema operacional usando o Winnt32.exe</span><span class="sxs-lookup"><span data-stu-id="846c7-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="846c7-123">Windows Update</span><span class="sxs-lookup"><span data-stu-id="846c7-123">Windows Update</span></span>

<span data-ttu-id="846c7-124">A substituição de arquivos protegidos por meios diferentes desses métodos especificados resulta na restauração dos arquivos originais pela WFP.</span><span class="sxs-lookup"><span data-stu-id="846c7-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 
