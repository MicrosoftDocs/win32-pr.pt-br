---
description: A ação MsiConfigureServices configura um serviço para o sistema. Essa ação consulta as tabelas MsiServiceConfig e MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Ação MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750607"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="5c8cb-104">Ação MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="5c8cb-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="5c8cb-105">A ação MsiConfigureServices configura um serviço para o sistema.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="5c8cb-106">Essa ação consulta as tabelas [MsiServiceConfig](msiserviceconfig-table.md) e [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8cb-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="5c8cb-107">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="5c8cb-108">Essa ação está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5c8cb-109">Os serviços do Windows fornecem a capacidade de executar automaticamente ações predefinidas em resposta a uma falha em um serviço.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="5c8cb-110">Para dar suporte à configuração dessas **ações de recuperação** programaticamente quando um serviço falha, o [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) foi adicionado ao msi na versão MSI 5,0.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="5c8cb-111">No entanto, essa funcionalidade não está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="5c8cb-112">Para solucionar esse problema, um desenvolvedor de aplicativos deve usar a funcionalidade de **ação personalizada** no MSI para executar **sc.exe** e definir as **Opções de recuperação** adequadamente.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="5c8cb-113">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="5c8cb-113">Sequence Restrictions</span></span>

<span data-ttu-id="5c8cb-114">Essa ação padrão deve ser usada na sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="5c8cb-115">Pararservices</span><span class="sxs-lookup"><span data-stu-id="5c8cb-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="5c8cb-116">Excluirservices</span><span class="sxs-lookup"><span data-stu-id="5c8cb-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="5c8cb-117">Qualquer uma das seguintes ações: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) ações.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="5c8cb-118">Instalarservices</span><span class="sxs-lookup"><span data-stu-id="5c8cb-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="5c8cb-119">MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="5c8cb-119">MsiConfigureServices</span></span>

[<span data-ttu-id="5c8cb-120">Iniciarservices</span><span class="sxs-lookup"><span data-stu-id="5c8cb-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="5c8cb-121">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="5c8cb-121">ActionData Messages</span></span>

<span data-ttu-id="5c8cb-122">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8cb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c8cb-123">Remarks</span></span>

<span data-ttu-id="5c8cb-124">Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para instalar serviços ou que o aplicativo faça parte de uma instalação gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5c8cb-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



