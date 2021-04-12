---
title: Detectando o status da instalação da instalação do Windows Media
description: Detectando o status da instalação da instalação do Windows Media
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player, detectando o status da instalação
- Windows Media Player, status da instalação
- Windows Media Player, redistribuindo software
- Windows Media Player, redistribuição de software
- detectando o status da instalação
- status da instalação
- redistribuindo software
- redistribuição de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364368"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="f883a-111">Detectando o status da instalação da instalação do Windows Media</span><span class="sxs-lookup"><span data-stu-id="f883a-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="f883a-112">O código a seguir pode ser usado com os pacotes de redistribuição do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f883a-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="f883a-113">O status da instalação é armazenado na entrada do registro **InstallResult** sob a seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="f883a-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="f883a-114">**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ instalação**</span><span class="sxs-lookup"><span data-stu-id="f883a-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="f883a-115">A entrada do registro **InstallResult** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="f883a-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="f883a-116">Nome</span><span class="sxs-lookup"><span data-stu-id="f883a-116">Name</span></span>              | <span data-ttu-id="f883a-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f883a-117">Type</span></span>           | <span data-ttu-id="f883a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f883a-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f883a-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="f883a-119">**InstallResult**</span></span> | <span data-ttu-id="f883a-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f883a-120">**REG\_DWORD**</span></span> | <span data-ttu-id="f883a-121">Um **HRESULT** que indica se a instalação do Windows Media Player foi bem-sucedida e se uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="f883a-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="f883a-122">Este é um código C++ de exemplo que pode ser incorporado a um aplicativo de instalação de chamada.</span><span class="sxs-lookup"><span data-stu-id="f883a-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="f883a-123">Esse código irá definir as `fSuccess` `fRebootNeeded` variáveis e como **true** ou **false**, conforme apropriado, com base no valor **HRESULT** gravado pela instalação do Windows Media Player no pacote de redistribuição de componentes.</span><span class="sxs-lookup"><span data-stu-id="f883a-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
 
// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
 
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="f883a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f883a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f883a-125">**Redistribuindo o software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="f883a-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




