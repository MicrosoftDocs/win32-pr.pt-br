---
description: O instalador executa ações personalizadas com privilégios de usuário por padrão para limitar o acesso de ações personalizadas ao sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Segurança de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297601"
---
# <a name="custom-action-security"></a><span data-ttu-id="f304b-103">Segurança de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f304b-103">Custom Action Security</span></span>

<span data-ttu-id="f304b-104">O instalador executa ações personalizadas com privilégios de usuário por padrão para limitar o acesso de ações personalizadas ao sistema.</span><span class="sxs-lookup"><span data-stu-id="f304b-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="f304b-105">O instalador pode executar ações personalizadas com privilégios elevados se um aplicativo gerenciado estiver sendo instalado ou se a política do sistema tiver sido especificada para privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="f304b-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="f304b-106">Você deve usar a propriedade [**MsiHiddenProperties**](msihiddenproperties.md) e **msidbCustomActionTypeHideTarget** para impedir o registro em log de informações confidenciais usadas pela ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="f304b-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="f304b-107">Para obter mais informações  sobre msidbCustomActionTypeHideTarget [, consulte opção de destino oculto de ação personalizada](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="f304b-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="f304b-108">Desmarque a propriedade CustomActionData depois de defini-la para garantir que os dados confidenciais não estejam mais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f304b-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="f304b-109">O código de exemplo abaixo é um trecho usado por uma ação personalizada de DLL imediata que está configurando dados para uso por uma ação personalizada adiada chamada "MyDeferredCA":</span><span class="sxs-lookup"><span data-stu-id="f304b-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



<span data-ttu-id="f304b-110">Observe que apenas [ações personalizadas de execução adiada](deferred-execution-custom-actions.md) podem usar o atributo **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="f304b-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="f304b-111">Para obter mais informações, consulte [ação personalizada In-Script opções de execução](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f304b-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="f304b-112">Se o bit **msidbCustomActionTypeNoImpersonate** não estiver definido para uma ação personalizada, o instalador executará a ação personalizada com privilégios de nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="f304b-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="f304b-113">Para obter mais informações, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f304b-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="f304b-114">Se o bit **msidbCustomActionTypeNoImpersonate** for definido e um aplicativo gerenciado estiver sendo instalado com a permissão de administrador, o instalador poderá executar a ação personalizada com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="f304b-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="f304b-115">No entanto, se um usuário tentar instalar o aplicativo gerenciado sem permissão de administrador, o instalador executará o aplicativo com privilégios de nível de usuário, independentemente de o **msidbCustomActionTypeNoImpersonate** ser definido.</span><span class="sxs-lookup"><span data-stu-id="f304b-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="f304b-116">Observe que uma ação personalizada pode ser executada com privilégios de sistema, mesmo quando o bit **msidbCustomActionTypeNoImpersonate** não está definido.</span><span class="sxs-lookup"><span data-stu-id="f304b-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="f304b-117">Isso ocorrerá se um administrador instalar o aplicativo para todos os usuários em um servidor que executa o serviço de função Terminal Server usando o Windows 2000 e a ação não estiver marcada com **msidbCustomActionTypeTSAware**.</span><span class="sxs-lookup"><span data-stu-id="f304b-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="f304b-118">Uma ação personalizada também pode ser executada com privilégios de sistema se a instalação for chamada quando não houver nenhum contexto de usuário.</span><span class="sxs-lookup"><span data-stu-id="f304b-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="f304b-119">Por exemplo, se não houver um usuário conectado no momento durante uma instalação invocada pela implantação de aplicativos do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f304b-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="f304b-120">Ao criar suas próprias ações personalizadas, você sempre deve criar a ação personalizada usando métodos seguros.</span><span class="sxs-lookup"><span data-stu-id="f304b-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="f304b-121">Para obter mais informações, consulte [diretrizes para proteger ações personalizadas](guidelines-for-securing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f304b-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



