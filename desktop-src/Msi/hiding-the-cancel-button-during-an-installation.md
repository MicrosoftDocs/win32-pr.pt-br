---
description: Você pode ocultar o botão Cancelar usado para cancelar uma instalação usando uma opção de linha de comando, a API do instalador Windows ou uma ação personalizada. O botão Cancelar pode ser oculto para parte ou toda a instalação, dependendo do método usado.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Ocultando o botão Cancelar durante uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b838803b65b8923dc45f36e17579e30114c1bc6d86c8fba2e533252e524568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129526"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a>Ocultando o botão Cancelar durante uma instalação

Você pode ocultar o **botão** Cancelar usado para cancelar uma instalação usando uma opção de linha de comando, a API do instalador Windows ou uma ação personalizada. O **botão** Cancelar pode ser oculto para parte ou toda a instalação, dependendo do método usado.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Ocultando o botão Cancelar da linha de comando

O **botão** Cancelar pode ser ocultado durante a instalação usando a opção de linha de comando (!). Isso só pode ser feito para uma instalação básica de nível de interface do usuário (/qb). O **botão** Cancelar fica oculto para toda a instalação. Para obter mais informações, consulte [Opções de linha de comando](command-line-options.md) e Interface do Usuário [níveis](user-interface-levels.md). A linha de comando a seguir oculta o **botão Cancelar** e instala Example.msi.

**msiexec /I example.msi /qb!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Ocultando o botão Cancelar de um aplicativo ou script

Você pode escrever um aplicativo ou script para ocultar o **botão** Cancelar. Isso só pode ser feito para uma instalação básica no nível da interface do usuário para que o **botão** Cancelar seja ocultado para toda a instalação.

Para ocultar o botão Cancelar de um aplicativo, de definido INSTALLUILEVEL \_ HIDECANCEL ao chamar [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). O exemplo a seguir oculta o **botão Cancelar** e instala Example.msi.


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



Para ocultar o **botão** Cancelar do script, adicione msiUILevelHideCancel à propriedade [**UILevel**](installer-uilevel.md) do [**Objeto do Instalador**](installer-object.md). O exemplo de VBScript a seguir oculta o **botão Cancelar** e instala Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Ocultando o botão Cancelar para partes de uma instalação usando uma ação personalizada

Sua instalação pode ocultar e  desabocar o botão Cancelar durante partes de uma instalação enviando uma mensagem INSTALLMESSAGE COMMONDATA usando uma ação ou \_ scripts personalizados da DLL. Para obter mais informações, consulte [Bibliotecas](dynamic-link-libraries.md) [](custom-actions.md)de vínculo dinâmico, [scripts,](scripts.md)ações personalizadas e Enviar mensagens para o instalador Windows [usando o MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Uma chamada para uma ação personalizada deve fornecer um registro. O campo 1 desse registro deve conter o valor 2 (dois) para especificar o **botão** Cancelar. O campo 2 deve conter o valor 0 ou 1. Um valor de 0 no Campo 2 oculta o botão e um valor de 1 no Campo 2 desaloca o botão. Observe que alocar um registro de tamanho 2 com [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fornece os campos 0, 1 e 2.

A ação personalizada da DLL de exemplo a seguir oculta o **botão** Cancelar.


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



A ação personalizada do VBScript a seguir oculta o **botão** Cancelar.


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



 

 



