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
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="4a417-103">APIs de interface do usuário sem fio</span><span class="sxs-lookup"><span data-stu-id="4a417-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="4a417-104">O Windows 8, o Windows Server 2012 e posterior incluem um novo recurso do Gerenciador de conexões que permite que os usuários se conectem facilmente à Internet e a outras redes (redes corporativas e domésticas, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="4a417-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="4a417-105">Esse novo recurso do Gerenciador de conexões substitui as interfaces de usuário **conectar-se a uma rede** e **gerenciar redes sem fio** incluídas em versões mais antigas do Windows para gerenciar conexões Wi-Fi nativas.</span><span class="sxs-lookup"><span data-stu-id="4a417-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="4a417-106">No Windows 7, no Windows Server 2008 e no Windows Vista, há várias interfaces do usuário (UIs) usadas para se conectar ou configurar uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="4a417-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="4a417-107">Essas interfaces do uso podem ser iniciadas em um aplicativo usando as funções nativas de Wi-Fi e Shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="4a417-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="4a417-108">Essas UIs não estão disponíveis no Windows 8, no Windows Server 2012 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a417-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="4a417-109">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Você não pode iniciar qualquer interface do usuário usada para se conectar ou configurar uma rede sem fio em um aplicativo programaticamente.</span><span class="sxs-lookup"><span data-stu-id="4a417-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="4a417-110">Conectar a uma rede</span><span class="sxs-lookup"><span data-stu-id="4a417-110">Connect to a network</span></span>

<span data-ttu-id="4a417-111">No Windows 8, no Windows Server 2012, no Windows 7, no Windows Server 2008 e no Windows Vista, o assistente **conectar-se a uma rede** pode ser usado para estabelecer uma conexão com uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="4a417-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="4a417-112">Você pode usar a função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar o assistente **conectar-se a uma rede** .</span><span class="sxs-lookup"><span data-stu-id="4a417-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="4a417-113">O código a seguir mostra uma chamada [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) que inicia o assistente **conectar a uma rede** .</span><span class="sxs-lookup"><span data-stu-id="4a417-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


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



## <a name="manage-wireless-networks"></a><span data-ttu-id="4a417-114">**Gerenciar redes sem fio**</span><span class="sxs-lookup"><span data-stu-id="4a417-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="4a417-115">No Windows 7, no Windows Server 2008 e no Windows Vista, o item **gerenciar redes sem fio** painel de controle é usado para gerenciar perfis de rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="4a417-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="4a417-116">A função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) também pode ser usada para iniciar o item **gerenciar redes sem fio** .</span><span class="sxs-lookup"><span data-stu-id="4a417-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="4a417-117">O caminho a ser usado ao chamar **ShellExecute** no Windows 7 e no Windows Vista é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4a417-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="4a417-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="4a417-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="4a417-119">O código de exemplo a seguir mostra como usar [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar o assistente de **redes sem fio gerenciadas** de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a417-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


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



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="4a417-120">Configurações avançadas para perfis de rede sem fio</span><span class="sxs-lookup"><span data-stu-id="4a417-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="4a417-121">O Windows Vista e versões posteriores incluem uma interface de usuário avançada que é usada para exibir e editar configurações avançadas de um perfil de rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="4a417-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="4a417-122">Você pode iniciar essa interface do usuário avançada chamando a função [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .</span><span class="sxs-lookup"><span data-stu-id="4a417-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a417-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a417-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a417-124">Usando WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="4a417-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="4a417-125">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="4a417-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="4a417-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="4a417-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="4a417-127">**WlanUIEditProfile**</span><span class="sxs-lookup"><span data-stu-id="4a417-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
