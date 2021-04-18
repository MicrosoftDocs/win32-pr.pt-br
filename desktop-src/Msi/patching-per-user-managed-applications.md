---
description: A partir do Windows Installer 3,0, é possível aplicar patches a um aplicativo que foi instalado em um contexto gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Aplicação de patch em aplicativos gerenciados por usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105778717"
---
# <a name="patching-per-user-managed-applications"></a><span data-ttu-id="2c454-103">Aplicação de patch em aplicativos gerenciados por usuário</span><span class="sxs-lookup"><span data-stu-id="2c454-103">Patching Per-User Managed Applications</span></span>

<span data-ttu-id="2c454-104">A partir do Windows Installer 3,0, é possível aplicar patches a um aplicativo que foi instalado em um contexto gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2c454-104">Beginning with Windows Installer 3.0, it is possible to apply patches to an application that has been installed in a per-user-managed context after the patch has been registered as having elevated privileges.</span></span>

<span data-ttu-id="2c454-105">**Windows Installer 2,0:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="2c454-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="2c454-106">Você não pode aplicar patches a aplicativos que estão instalados em um contexto gerenciado por usuário usando versões do Windows Installer anteriores ao Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="2c454-106">You cannot apply patches to applications that are installed in a per-user managed context using versions of Windows Installer earlier than Windows Installer 3.0.</span></span>

<span data-ttu-id="2c454-107">Um aplicativo é instalado no estado gerenciado por usuário nos seguintes casos.</span><span class="sxs-lookup"><span data-stu-id="2c454-107">An application is installed in the per-user-managed state in the following cases.</span></span>

-   <span data-ttu-id="2c454-108">A instalação por usuário do aplicativo foi executada usando a implantação e [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="2c454-108">The per-user installation of the application was performed using deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span>
-   <span data-ttu-id="2c454-109">O aplicativo foi anunciado para um usuário especificado e instalado pelo método descrito em [anunciar um aplicativo Per-User a ser instalado com privilégios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="2c454-109">The application was advertised to a specified user and installed by the method described in [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>

<span data-ttu-id="2c454-110">São necessários privilégios para instalar um aplicativo no contexto gerenciado por usuário; Portanto, futuras Windows Installer reinstalações ou reparos do aplicativo também são executadas pelo instalador usando privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2c454-110">Privileges are required to install an application in the per-user-managed context; therefore, future Windows Installer reinstallations or repairs of the application are also performed by the installer using elevated privileges.</span></span> <span data-ttu-id="2c454-111">Isso significa que somente os patches de fontes confiáveis podem ser aplicados ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c454-111">This means that only patches from trusted sources can be applied to the application.</span></span>

<span data-ttu-id="2c454-112">A partir do Windows Installer 3,0, você pode aplicar um patch a um aplicativo gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2c454-112">Beginning with Windows Installer 3.0, you can apply a patch to a per-user managed application after the patch has been registered as having elevated privileges.</span></span> <span data-ttu-id="2c454-113">Para registrar um patch como tendo privilégios elevados, use a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) ou o método [**SourceListAddSource**](patch-sourcelistaddsource.md) do objeto [**patch**](patch-object.md) , com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2c454-113">To register a patch as having elevated privileges, use the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function or the [**SourceListAddSource**](patch-sourcelistaddsource.md) method of the [**Patch**](patch-object.md) object, with elevated privileges.</span></span> <span data-ttu-id="2c454-114">Depois de registrar o patch, você pode aplicar o patch usando as funções [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , os métodos [**ApplyPatch**](installer-applypatch.md) ou [**ApplyMultiplePatches**](installer-applymultiplepatches.md) do [**objeto instalador**](installer-object.md)ou a opção de [linha de comando](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="2c454-114">After registering the patch, you can apply the patch using the [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) functions, [**ApplyPatch**](installer-applypatch.md) or [**ApplyMultiplePatches**](installer-applymultiplepatches.md) methods of the [**Installer Object**](installer-object.md), or the /p [command-line option](command-line-options.md).</span></span>

> [!Note]
> <span data-ttu-id="2c454-115">Um patch pode ser registrado como tendo privilégios elevados antes de o aplicativo ser instalado.</span><span class="sxs-lookup"><span data-stu-id="2c454-115">A patch can be registered as having elevated privileges before the application is installed.</span></span> <span data-ttu-id="2c454-116">Quando um patch é registrado, ele permanece registrado até que o último aplicativo registrado para esse patch seja removido.</span><span class="sxs-lookup"><span data-stu-id="2c454-116">When a patch has been registered, it remains registered until the last registered application for this patch is removed.</span></span>
> 
> <span data-ttu-id="2c454-117">Os patches que foram aplicados a um aplicativo gerenciado por usuário não podem ser removidos sem a remoção do aplicativo inteiro.</span><span class="sxs-lookup"><span data-stu-id="2c454-117">Patches that have been applied to a per-user managed application cannot be removed without removing the entire application.</span></span> <span data-ttu-id="2c454-118">Os registros de patch para um aplicativo gerenciado por usuário são removidos na remoção do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c454-118">The patch registrations for a per-user managed application are removed on the removal of the application.</span></span>

<span data-ttu-id="2c454-119">Você também pode usar esse método para permitir que um não administrador corrija um aplicativo por computador ou pode usar a aplicação de patches com privilégios mínimos descritas na [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="2c454-119">You can also use this method to enable a non-administrator to patch a per-machine application, or you can use least-privilege patching described in [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="example-1"></a><span data-ttu-id="2c454-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c454-120">Example 1</span></span>

<span data-ttu-id="2c454-121">O exemplo de script a seguir usa o método [**SourceListAddSource**](patch-sourcelistaddsource.md) para registrar um pacote de patch localizado em \\ \\ Server \\ share \\ Products \\ patches \\ example. msp como tendo privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2c454-121">The following scripting sample uses the [**SourceListAddSource**](patch-sourcelistaddsource.md) method to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="2c454-122">Esse patch está pronto para ser aplicado a um produto gerenciado por usuário.</span><span class="sxs-lookup"><span data-stu-id="2c454-122">That patch is then ready to be applied to a per-user managed product.</span></span>

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a><span data-ttu-id="2c454-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2c454-123">Example 2</span></span>

<span data-ttu-id="2c454-124">O exemplo de código a seguir usa a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar um pacote de patch localizado em \\ \\ Server \\ share \\ Products \\ patches \\ example. msp como tendo privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2c454-124">The following code sample uses the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="2c454-125">Esse patch está pronto para ser aplicado a um produto gerenciado por usuário.</span><span class="sxs-lookup"><span data-stu-id="2c454-125">That patch is then ready to be applied to a per-user managed product.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
