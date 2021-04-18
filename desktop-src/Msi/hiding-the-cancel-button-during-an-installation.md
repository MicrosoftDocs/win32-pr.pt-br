---
description: Você pode ocultar o botão Cancelar que é usado para cancelar uma instalação usando uma opção de linha de comando, a API Windows Installer ou uma ação personalizada. O botão Cancelar pode ser ocultado para parte ou para toda a instalação, dependendo do método usado.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Ocultando o botão Cancelar durante uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749800"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="fc7c1-104">Ocultando o botão Cancelar durante uma instalação</span><span class="sxs-lookup"><span data-stu-id="fc7c1-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="fc7c1-105">Você pode ocultar o botão **Cancelar** que é usado para cancelar uma instalação usando uma opção de linha de comando, a API Windows Installer ou uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="fc7c1-106">O botão **Cancelar** pode ser ocultado para parte ou para toda a instalação, dependendo do método usado.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="fc7c1-107">Ocultando o botão Cancelar da linha de comando</span><span class="sxs-lookup"><span data-stu-id="fc7c1-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="fc7c1-108">O botão **Cancelar** pode ser ocultado durante a instalação usando a opção de linha de comando (!).</span><span class="sxs-lookup"><span data-stu-id="fc7c1-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="fc7c1-109">Isso só pode ser feito para uma instalação básica no nível da interface do usuário (/QB).</span><span class="sxs-lookup"><span data-stu-id="fc7c1-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="fc7c1-110">O botão **Cancelar** está oculto para toda a instalação.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="fc7c1-111">Para obter mais informações, consulte [Opções de linha de comando](command-line-options.md) e níveis de interface do [usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="fc7c1-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="fc7c1-112">A linha de comando a seguir oculta o botão **Cancelar** e instala Example.msi.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="fc7c1-113">**msiexec/I example.msi/QB!**</span><span class="sxs-lookup"><span data-stu-id="fc7c1-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="fc7c1-114">Ocultando o botão Cancelar de um aplicativo ou script</span><span class="sxs-lookup"><span data-stu-id="fc7c1-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="fc7c1-115">Você pode escrever um aplicativo ou script para ocultar o botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="fc7c1-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="fc7c1-116">Isso só pode ser feito para uma instalação básica no nível da interface do usuário para que o botão **Cancelar** fique oculto em toda a instalação.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="fc7c1-117">Para ocultar o botão de cancelamento de um aplicativo, defina INSTALLUILEVEL \_ HIDECANCEL ao chamar [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="fc7c1-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="fc7c1-118">O exemplo a seguir oculta o botão **Cancelar** e instala Example.msi.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



<span data-ttu-id="fc7c1-119">Para ocultar o botão **Cancelar** do script, adicione msiUILevelHideCancel à propriedade [**UILevel**](installer-uilevel.md) do objeto do [**instalador**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="fc7c1-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="fc7c1-120">O exemplo de VBScript a seguir oculta o botão **Cancelar** e instala Example.msi.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="fc7c1-121">Ocultando o botão Cancelar para partes de uma instalação usando uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="fc7c1-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="fc7c1-122">Sua instalação pode ocultar e reexibir o botão **Cancelar** durante partes de uma instalação enviando uma mensagem INSTALLMESSAGE \_ COMMONDATA usando uma ação personalizada de dll ou scripts.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="fc7c1-123">Para obter mais informações, consulte [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md), [scripts](scripts.md), [ações personalizadas](custom-actions.md)e [envio de mensagens para Windows Installer usando o MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="fc7c1-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="fc7c1-124">Uma chamada para uma ação personalizada deve fornecer um registro.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="fc7c1-125">O campo 1 deste registro deve conter o valor 2 (dois) para especificar o botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="fc7c1-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="fc7c1-126">O campo 2 deve conter o valor 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="fc7c1-127">Um valor de 0 no campo 2 oculta o botão e um valor de 1 no campo 2 Reexibe o botão.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="fc7c1-128">Observe que alocar um registro de tamanho 2 com [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fornece os campos 0, 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="fc7c1-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="fc7c1-129">A ação personalizada de DLL de exemplo a seguir oculta o botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="fc7c1-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



<span data-ttu-id="fc7c1-130">A ação personalizada do VBScript a seguir oculta o botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="fc7c1-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



