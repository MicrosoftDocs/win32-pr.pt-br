---
description: A partir do Windows Installer 3,0, é possível desinstalar alguns patches dos aplicativos.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Desinstalando patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172163"
---
# <a name="uninstalling-patches"></a>Desinstalando patches

A partir do Windows Installer 3,0, é possível desinstalar alguns patches dos aplicativos. O patch deve ser um [patch desinstalável](uninstallable-patches.md). Ao usar uma versão Windows Installer inferior à versão 3,0, a [remoção de patches](removing-patches.md) exige a desinstalação do produto de patch e a reinstalação do produto sem aplicar o patch.

**Windows Installer 2,0:** Sem suporte. Os patches aplicados usando uma versão do Windows Installer que é anterior ao Windows Installer 3,0 não são desinstaláveis.

Quando você invoca uma desinstalação de um patch por qualquer um dos métodos a seguir, o instalador tenta remover o patch do primeiro produto visível para o aplicativo ou usuário que está solicitando a desinstalação. O instalador procura produtos com patch na seguinte ordem: gerenciado por usuário, não gerenciado por usuário, por máquina.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Desinstalando um patch usando o MSIPATCHREMOVE em uma linha de comando

Você pode desinstalar os patches de um comando usando msiexec.exe e as [Opções de linha de comando](command-line-options.md). A linha de comando de exemplo a seguir remove um [patch desinstalável](uninstallable-patches.md), example. msp, de um aplicativo, example.msi, usando a propriedade [**MSIPATCHREMOVE**](msipatchremove.md) e a opção de linha de comando/i. Ao usar/i, o aplicativo com patch pode ser identificado pelo caminho para o pacote do aplicativo (arquivo. msi) ou o [código do produto](product-codes.md)do aplicativo. Neste exemplo, o pacote de instalação do aplicativo está localizado no " \\ \\ exemplo de produtos de compartilhamento de servidor \\ \\ \\ \\example.msi" e a propriedade [**ProductCode**](productcode.md) do aplicativo é "{0C9840E7-7F0B-C648-10F0-4641926FE463}". O pacote de patch está localizado em " \\ \\ Server \\ share \\ Products \\ example \\ patches \\ example. msp" e o GUID do código do patch é "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".

**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Desinstalando um patch usando as opções de linha de comando padrão

A partir do Windows Installer versão 3,0, você pode usar as [Opções de linha de comando padrão](standard-installer-command-line-options.md) usadas pelas atualizações do sistema operacional Microsoft Windows (update.exe) para desinstalar os patches Windows Installer de uma linha de comando.

A linha de comando a seguir é o equivalente de linha de comando padrão da linha de comando Windows Installer usada para desinstalar um patch usando a propriedade [**MSIPATCHREMOVE**](msipatchremove.md) . A opção/Uninstall usada com a opção/pacote denota a desinstalação de um patch. O patch pode ser referenciado pelo caminho completo para o patch ou pelo GUID do código do patch.

**Msiexec/pacote {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/Passive**

> [!Note]  
> A opção/passive Standard não é um equivalente exato da opção Windows Installer/QB.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Desinstalando um patch usando o método RemovePatches

Você pode desinstalar patches do script usando a [interface de automação](automation-interface.md)de Windows Installer. O exemplo de script a seguir remove um [patch desinstalável](uninstallable-patches.md), example. msp, de um aplicativo, example.msi, usando o método [**RemovePatches**](installer-removepatches.md) do objeto do [instalador](installer-object.md) . Cada patch que está sendo desinstalado pode ser representado pelo caminho completo para o pacote de patch ou pelo GUID de código do patch. Neste exemplo, o pacote de instalação do aplicativo está localizado no " \\ \\ exemplo de produtos de compartilhamento de servidor \\ \\ \\ \\example.msi" e a propriedade [**ProductCode**](productcode.md) do aplicativo é "{0C9840E7-7F0B-C648-10F0-4641926FE463}". O pacote de patch está localizado em " \\ \\ Server \\ share \\ Products \\ example \\ patches \\ example. msp" e o GUID do código do patch é "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Desinstalando um patch usando Adicionar/remover programas

Com o Windows XP, você pode desinstalar os patches usando Adicionar ou remover programas.

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Desinstalando um patch usando a função MsiRemovePatches

Seus aplicativos podem desinstalar patches de outros aplicativos usando as [funções Windows Installer](installer-functions.md). O exemplo de código a seguir remove um [patch não instalável](uninstallable-patches.md), example. msp, de um aplicativo, example.msi, usando a função [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) . Um patch pode ser referenciado pelo caminho completo para o pacote de patch ou pelo GUID de código do patch. Neste exemplo, o pacote de instalação do aplicativo está localizado no " \\ \\ exemplo de produtos de compartilhamento de servidor \\ \\ \\ \\example.msi" e a propriedade [**ProductCode**](productcode.md) do aplicativo é "{0C9840E7-7F0B-C648-10F0-4641926FE463}". O pacote de patch está localizado em " \\ \\ Server \\ share \\ Products \\ example \\ patches \\ example. msp" e o GUID do código do patch é "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Desinstalando um patch de todos os aplicativos usando a função MsiRemovePatches

Um único patch pode atualizar mais de um produto no computador. Um aplicativo pode usar o [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar todos os produtos no computador e determinar se um patch foi aplicado a uma determinada instância do produto. O aplicativo pode, então, desinstalar o patch usando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa). Por exemplo, um único patch pode atualizar vários produtos se o patch atualizar um arquivo em um componente compartilhado por vários produtos e o patch for distribuído para atualizar ambos os produtos.

O exemplo a seguir demonstra como um aplicativo pode usar o Windows Installer para remover um patch de todos os aplicativos que estão disponíveis para o usuário. Ele não remove o patch dos aplicativos instalados por usuário para outro usuário.


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequenciamento de patch](sequencing-patches.md)
</dt> <dt>

[Removendo patches](removing-patches.md)
</dt> <dt>

[Patches desinstaláveis](uninstallable-patches.md)
</dt> <dt>

[Corrigir ações personalizadas de desinstalação de patch](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



