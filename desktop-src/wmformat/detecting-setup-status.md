---
title: Detectando o status da instalação
description: Detectando o status da instalação
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- SDK do Windows Media Format, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- SDK do Windows Media Format, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, detectando o status da instalação
- redistribuição, detectando o status da instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637141"
---
# <a name="detecting-setup-status"></a><span data-ttu-id="810ba-111">Detectando o status da instalação</span><span class="sxs-lookup"><span data-stu-id="810ba-111">Detecting Setup Status</span></span>

<span data-ttu-id="810ba-112">Quando o executável de redistribuição é executado em um computador, ele registra seu status de instalação no registro como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="810ba-112">When the redistribution executable runs on a computer, it records its installation status in the registry as an **HRESULT** value.</span></span> <span data-ttu-id="810ba-113">O status da instalação é armazenado na entrada do registro **InstallResult** sob a seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="810ba-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="810ba-114">**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ instalação**</span><span class="sxs-lookup"><span data-stu-id="810ba-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="810ba-115">A entrada do registro **InstallResult** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="810ba-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="810ba-116">Nome</span><span class="sxs-lookup"><span data-stu-id="810ba-116">Name</span></span>              | <span data-ttu-id="810ba-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="810ba-117">Type</span></span>           | <span data-ttu-id="810ba-118">Valor</span><span class="sxs-lookup"><span data-stu-id="810ba-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810ba-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="810ba-119">**InstallResult**</span></span> | <span data-ttu-id="810ba-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="810ba-120">**REG\_DWORD**</span></span> | <span data-ttu-id="810ba-121">Um **HRESULT** que indica se a instalação do Windows Media Player foi bem-sucedida e se uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="810ba-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="810ba-122">O código a seguir definirá as variáveis *fSucess* e *fRebootNeeded* como **true** ou **false**, conforme apropriado, com base no valor **HRESULT** gravado pela instalação do Windows Media no pacote de redistribuição de componentes.</span><span class="sxs-lookup"><span data-stu-id="810ba-122">The following code will set the *fSucess* and *fRebootNeeded* variables to **True** or **False**, as appropriate, based on the **HRESULT** value written by Windows Media setup in the component redistribution package.</span></span>


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

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="810ba-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="810ba-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="810ba-124">**Redistribuição de software**</span><span class="sxs-lookup"><span data-stu-id="810ba-124">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




