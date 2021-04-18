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
# <a name="hiding-the-cancel-button-during-an-installation"></a>Ocultando o botão Cancelar durante uma instalação

Você pode ocultar o botão **Cancelar** que é usado para cancelar uma instalação usando uma opção de linha de comando, a API Windows Installer ou uma ação personalizada. O botão **Cancelar** pode ser ocultado para parte ou para toda a instalação, dependendo do método usado.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Ocultando o botão Cancelar da linha de comando

O botão **Cancelar** pode ser ocultado durante a instalação usando a opção de linha de comando (!). Isso só pode ser feito para uma instalação básica no nível da interface do usuário (/QB). O botão **Cancelar** está oculto para toda a instalação. Para obter mais informações, consulte [Opções de linha de comando](command-line-options.md) e níveis de interface do [usuário](user-interface-levels.md). A linha de comando a seguir oculta o botão **Cancelar** e instala Example.msi.

**msiexec/I example.msi/QB!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Ocultando o botão Cancelar de um aplicativo ou script

Você pode escrever um aplicativo ou script para ocultar o botão **Cancelar** . Isso só pode ser feito para uma instalação básica no nível da interface do usuário para que o botão **Cancelar** fique oculto em toda a instalação.

Para ocultar o botão de cancelamento de um aplicativo, defina INSTALLUILEVEL \_ HIDECANCEL ao chamar [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). O exemplo a seguir oculta o botão **Cancelar** e instala Example.msi.


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



Para ocultar o botão **Cancelar** do script, adicione msiUILevelHideCancel à propriedade [**UILevel**](installer-uilevel.md) do objeto do [**instalador**](installer-object.md). O exemplo de VBScript a seguir oculta o botão **Cancelar** e instala Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Ocultando o botão Cancelar para partes de uma instalação usando uma ação personalizada

Sua instalação pode ocultar e reexibir o botão **Cancelar** durante partes de uma instalação enviando uma mensagem INSTALLMESSAGE \_ COMMONDATA usando uma ação personalizada de dll ou scripts. Para obter mais informações, consulte [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md), [scripts](scripts.md), [ações personalizadas](custom-actions.md)e [envio de mensagens para Windows Installer usando o MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Uma chamada para uma ação personalizada deve fornecer um registro. O campo 1 deste registro deve conter o valor 2 (dois) para especificar o botão **Cancelar** . O campo 2 deve conter o valor 0 ou 1. Um valor de 0 no campo 2 oculta o botão e um valor de 1 no campo 2 Reexibe o botão. Observe que alocar um registro de tamanho 2 com [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fornece os campos 0, 1 e 2.

A ação personalizada de DLL de exemplo a seguir oculta o botão **Cancelar** .


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



A ação personalizada do VBScript a seguir oculta o botão **Cancelar** .


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



 

 



