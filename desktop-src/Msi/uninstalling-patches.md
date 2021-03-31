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
# <a name="uninstalling-patches"></a><span data-ttu-id="badf7-103">Desinstalando patches</span><span class="sxs-lookup"><span data-stu-id="badf7-103">Uninstalling Patches</span></span>

<span data-ttu-id="badf7-104">A partir do Windows Installer 3,0, é possível desinstalar alguns patches dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="badf7-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="badf7-105">O patch deve ser um [patch desinstalável](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="badf7-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="badf7-106">Ao usar uma versão Windows Installer inferior à versão 3,0, a [remoção de patches](removing-patches.md) exige a desinstalação do produto de patch e a reinstalação do produto sem aplicar o patch.</span><span class="sxs-lookup"><span data-stu-id="badf7-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="badf7-107">**Windows Installer 2,0:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="badf7-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="badf7-108">Os patches aplicados usando uma versão do Windows Installer que é anterior ao Windows Installer 3,0 não são desinstaláveis.</span><span class="sxs-lookup"><span data-stu-id="badf7-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="badf7-109">Quando você invoca uma desinstalação de um patch por qualquer um dos métodos a seguir, o instalador tenta remover o patch do primeiro produto visível para o aplicativo ou usuário que está solicitando a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="badf7-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="badf7-110">O instalador procura produtos com patch na seguinte ordem: gerenciado por usuário, não gerenciado por usuário, por máquina.</span><span class="sxs-lookup"><span data-stu-id="badf7-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="badf7-111">Desinstalando um patch usando o MSIPATCHREMOVE em uma linha de comando</span><span class="sxs-lookup"><span data-stu-id="badf7-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="badf7-112">Você pode desinstalar os patches de um comando usando msiexec.exe e as [Opções de linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="badf7-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="badf7-113">A linha de comando de exemplo a seguir remove um [patch desinstalável](uninstallable-patches.md), example. msp, de um aplicativo, example.msi, usando a propriedade [**MSIPATCHREMOVE**](msipatchremove.md) e a opção de linha de comando/i.</span><span class="sxs-lookup"><span data-stu-id="badf7-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="badf7-114">Ao usar/i, o aplicativo com patch pode ser identificado pelo caminho para o pacote do aplicativo (arquivo. msi) ou o [código do produto](product-codes.md)do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="badf7-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="badf7-115">Neste exemplo, o pacote de instalação do aplicativo está localizado no " \\ \\ exemplo de produtos de compartilhamento de servidor \\ \\ \\ \\example.msi" e a propriedade [**ProductCode**](productcode.md) do aplicativo é "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="badf7-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="badf7-116">O pacote de patch está localizado em " \\ \\ Server \\ share \\ Products \\ example \\ patches \\ example. msp" e o GUID do código do patch é "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="badf7-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="badf7-117">**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**</span><span class="sxs-lookup"><span data-stu-id="badf7-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="badf7-118">Desinstalando um patch usando as opções de linha de comando padrão</span><span class="sxs-lookup"><span data-stu-id="badf7-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="badf7-119">A partir do Windows Installer versão 3,0, você pode usar as [Opções de linha de comando padrão](standard-installer-command-line-options.md) usadas pelas atualizações do sistema operacional Microsoft Windows (update.exe) para desinstalar os patches Windows Installer de uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="badf7-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="badf7-120">A linha de comando a seguir é o equivalente de linha de comando padrão da linha de comando Windows Installer usada para desinstalar um patch usando a propriedade [**MSIPATCHREMOVE**](msipatchremove.md) .</span><span class="sxs-lookup"><span data-stu-id="badf7-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="badf7-121">A opção/Uninstall usada com a opção/pacote denota a desinstalação de um patch.</span><span class="sxs-lookup"><span data-stu-id="badf7-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="badf7-122">O patch pode ser referenciado pelo caminho completo para o patch ou pelo GUID do código do patch.</span><span class="sxs-lookup"><span data-stu-id="badf7-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="badf7-123">**Msiexec/pacote {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/Passive**</span><span class="sxs-lookup"><span data-stu-id="badf7-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="badf7-124">A opção/passive Standard não é um equivalente exato da opção Windows Installer/QB.</span><span class="sxs-lookup"><span data-stu-id="badf7-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="badf7-125">Desinstalando um patch usando o método RemovePatches</span><span class="sxs-lookup"><span data-stu-id="badf7-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="badf7-126">Você pode desinstalar patches do script usando a [interface de automação](automation-interface.md)de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="badf7-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="badf7-127">O exemplo de script a seguir remove um [patch desinstalável](uninstallable-patches.md), example. msp, de um aplicativo, example.msi, usando o método [**RemovePatches**](installer-removepatches.md) do objeto do [instalador](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="badf7-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="badf7-128">Cada patch que está sendo desinstalado pode ser representado pelo caminho completo para o pacote de patch ou pelo GUID de código do patch.</span><span class="sxs-lookup"><span data-stu-id="badf7-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="badf7-129">Neste exemplo, o pacote de instalação do aplicativo está localizado no " \\ \\ exemplo de produtos de compartilhamento de servidor \\ \\ \\ \\example.msi" e a propriedade [**ProductCode**](productcode.md) do aplicativo é "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="badf7-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="badf7-130">O pacote de patch está localizado em " \\ \\ Server \\ share \\ Products \\ example \\ patches \\ example. msp" e o GUID do código do patch é "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="badf7-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="badf7-131">Desinstalando um patch usando Adicionar/remover programas</span><span class="sxs-lookup"><span data-stu-id="badf7-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="badf7-132">Com o Windows XP, você pode desinstalar os patches usando Adicionar ou remover programas.</span><span class="sxs-lookup"><span data-stu-id="badf7-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="badf7-133">Desinstalando um patch usando a função MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="badf7-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="badf7-134">Seus aplicativos podem desinstalar patches de outros aplicativos usando as [funções Windows Installer](installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="badf7-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="badf7-135">O exemplo de código a seguir remove um [patch não instalável](uninstallable-patches.md), example. msp, de um aplicativo, example.msi, usando a função [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) .</span><span class="sxs-lookup"><span data-stu-id="badf7-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="badf7-136">Um patch pode ser referenciado pelo caminho completo para o pacote de patch ou pelo GUID de código do patch.</span><span class="sxs-lookup"><span data-stu-id="badf7-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="badf7-137">Neste exemplo, o pacote de instalação do aplicativo está localizado no " \\ \\ exemplo de produtos de compartilhamento de servidor \\ \\ \\ \\example.msi" e a propriedade [**ProductCode**](productcode.md) do aplicativo é "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="badf7-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="badf7-138">O pacote de patch está localizado em " \\ \\ Server \\ share \\ Products \\ example \\ patches \\ example. msp" e o GUID do código do patch é "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="badf7-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="badf7-139">Desinstalando um patch de todos os aplicativos usando a função MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="badf7-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="badf7-140">Um único patch pode atualizar mais de um produto no computador.</span><span class="sxs-lookup"><span data-stu-id="badf7-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="badf7-141">Um aplicativo pode usar o [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar todos os produtos no computador e determinar se um patch foi aplicado a uma determinada instância do produto.</span><span class="sxs-lookup"><span data-stu-id="badf7-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="badf7-142">O aplicativo pode, então, desinstalar o patch usando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="badf7-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="badf7-143">Por exemplo, um único patch pode atualizar vários produtos se o patch atualizar um arquivo em um componente compartilhado por vários produtos e o patch for distribuído para atualizar ambos os produtos.</span><span class="sxs-lookup"><span data-stu-id="badf7-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="badf7-144">O exemplo a seguir demonstra como um aplicativo pode usar o Windows Installer para remover um patch de todos os aplicativos que estão disponíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="badf7-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="badf7-145">Ele não remove o patch dos aplicativos instalados por usuário para outro usuário.</span><span class="sxs-lookup"><span data-stu-id="badf7-145">It does not remove the patch from applications installed per-user for another user.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="badf7-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="badf7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="badf7-147">Sequenciamento de patch</span><span class="sxs-lookup"><span data-stu-id="badf7-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="badf7-148">Removendo patches</span><span class="sxs-lookup"><span data-stu-id="badf7-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="badf7-149">Patches desinstaláveis</span><span class="sxs-lookup"><span data-stu-id="badf7-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="badf7-150">Corrigir ações personalizadas de desinstalação de patch</span><span class="sxs-lookup"><span data-stu-id="badf7-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="badf7-151">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="badf7-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="badf7-152">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="badf7-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="badf7-153">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="badf7-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="badf7-154">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="badf7-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



