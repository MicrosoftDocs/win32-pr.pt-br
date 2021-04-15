---
description: O Windows 8, o Windows Server 2012 e posterior incluem um novo recurso do Gerenciador de conexões que permite que os usuários se conectem facilmente à Internet e a outras redes (redes corporativas e domésticas, por exemplo).
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: APIs de interface do usuário sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506275"
---
# <a name="wireless-user-interface-apis"></a>APIs de interface do usuário sem fio

O Windows 8, o Windows Server 2012 e posterior incluem um novo recurso do Gerenciador de conexões que permite que os usuários se conectem facilmente à Internet e a outras redes (redes corporativas e domésticas, por exemplo). Esse novo recurso do Gerenciador de conexões substitui as interfaces de usuário **conectar-se a uma rede** e **gerenciar redes sem fio** incluídas em versões mais antigas do Windows para gerenciar conexões Wi-Fi nativas.

No Windows 7, no Windows Server 2008 e no Windows Vista, há várias interfaces do usuário (UIs) usadas para se conectar ou configurar uma rede sem fio. Essas interfaces do uso podem ser iniciadas em um aplicativo usando as funções nativas de Wi-Fi e Shell do Windows. Essas UIs não estão disponíveis no Windows 8, no Windows Server 2012 e versões posteriores.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Você não pode iniciar qualquer interface do usuário usada para se conectar ou configurar uma rede sem fio em um aplicativo programaticamente.

## <a name="connect-to-a-network"></a>Conectar a uma rede

No Windows 8, no Windows Server 2012, no Windows 7, no Windows Server 2008 e no Windows Vista, o assistente **conectar-se a uma rede** pode ser usado para estabelecer uma conexão com uma rede sem fio. Você pode usar a função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar o assistente **conectar-se a uma rede** .

O código a seguir mostra uma chamada [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) que inicia o assistente **conectar a uma rede** .


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a>**Gerenciar redes sem fio**

No Windows 7, no Windows Server 2008 e no Windows Vista, o item **gerenciar redes sem fio** painel de controle é usado para gerenciar perfis de rede sem fio. A função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) também pode ser usada para iniciar o item **gerenciar redes sem fio** . O caminho a ser usado ao chamar **ShellExecute** no Windows 7 e no Windows Vista é o seguinte:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

O código de exemplo a seguir mostra como usar [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar o assistente de **redes sem fio gerenciadas** de um aplicativo.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a>Configurações avançadas para perfis de rede sem fio

O Windows Vista e versões posteriores incluem uma interface de usuário avançada que é usada para exibir e editar configurações avançadas de um perfil de rede sem fio. Você pode iniciar essa interface do usuário avançada chamando a função [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando WiFi nativo](using-native-wifi.md)
</dt> <dt>

[Exemplos de perfil sem fio](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
