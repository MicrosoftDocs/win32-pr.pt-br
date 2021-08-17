---
description: a partir do Windows Installer 3,0, é possível aplicar patches a um aplicativo que foi instalado em um contexto gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Aplicação de patch em aplicativos gerenciados por usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516af282dc7f149b86d03192303dc1b3da14416d1a6a22a4f3e716f641777500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979366"
---
# <a name="patching-per-user-managed-applications"></a>Aplicação de patch em aplicativos gerenciados por usuário

a partir do Windows Installer 3,0, é possível aplicar patches a um aplicativo que foi instalado em um contexto gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados.

**Windows Installer 2,0:** Sem suporte. você não pode aplicar patches a aplicativos que estão instalados em um contexto gerenciado por usuário usando versões do Windows Installer anteriores ao Windows Installer 3,0.

Um aplicativo é instalado no estado gerenciado por usuário nos seguintes casos.

-   A instalação por usuário do aplicativo foi executada usando a implantação e [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page).
-   O aplicativo foi anunciado para um usuário especificado e instalado pelo método descrito em [anunciar um aplicativo Per-User a ser instalado com privilégios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).

São necessários privilégios para instalar um aplicativo no contexto gerenciado por usuário; portanto, futuras Windows Installer reinstalações ou reparos do aplicativo também são executadas pelo instalador usando privilégios elevados. Isso significa que somente os patches de fontes confiáveis podem ser aplicados ao aplicativo.

a partir do Windows Installer 3,0, você pode aplicar um patch a um aplicativo gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados. Para registrar um patch como tendo privilégios elevados, use a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) ou o método [**SourceListAddSource**](patch-sourcelistaddsource.md) do objeto [**patch**](patch-object.md) , com privilégios elevados. Depois de registrar o patch, você pode aplicar o patch usando as funções [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , os métodos [**ApplyPatch**](installer-applypatch.md) ou [**ApplyMultiplePatches**](installer-applymultiplepatches.md) do [**objeto instalador**](installer-object.md)ou a opção de [linha de comando](command-line-options.md)/p.

> [!Note]
> Um patch pode ser registrado como tendo privilégios elevados antes de o aplicativo ser instalado. Quando um patch é registrado, ele permanece registrado até que o último aplicativo registrado para esse patch seja removido.
> 
> Os patches que foram aplicados a um aplicativo gerenciado por usuário não podem ser removidos sem a remoção do aplicativo inteiro. Os registros de patch para um aplicativo gerenciado por usuário são removidos na remoção do aplicativo.

Você também pode usar esse método para permitir que um não administrador corrija um aplicativo por computador ou pode usar a aplicação de patches com privilégios mínimos descritas na [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md).

## <a name="example-1"></a>Exemplo 1

O exemplo de script a seguir usa o método [**SourceListAddSource**](patch-sourcelistaddsource.md) para registrar um pacote de patch localizado em \\ \\ Server \\ share \\ Products \\ patches \\ example. msp como tendo privilégios elevados. Esse patch está pronto para ser aplicado a um produto gerenciado por usuário.

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

## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir usa a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar um pacote de patch localizado em \\ \\ Server \\ share \\ Products \\ patches \\ example. msp como tendo privilégios elevados. Esse patch está pronto para ser aplicado a um produto gerenciado por usuário.


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



 

 
