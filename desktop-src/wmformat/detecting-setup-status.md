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
# <a name="detecting-setup-status"></a>Detectando o status da instalação

Quando o executável de redistribuição é executado em um computador, ele registra seu status de instalação no registro como um valor **HRESULT** . O status da instalação é armazenado na entrada do registro **InstallResult** sob a seguinte subchave:

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ instalação**

A entrada do registro **InstallResult** tem o seguinte formato.



| Nome              | Type           | Valor                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Um **HRESULT** que indica se a instalação do Windows Media Player foi bem-sucedida e se uma reinicialização é necessária. |



 

O código a seguir definirá as variáveis *fSucess* e *fRebootNeeded* como **true** ou **false**, conforme apropriado, com base no valor **HRESULT** gravado pela instalação do Windows Media no pacote de redistribuição de componentes.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuição de software**](software-redistribution.md)
</dt> </dl>

 

 




