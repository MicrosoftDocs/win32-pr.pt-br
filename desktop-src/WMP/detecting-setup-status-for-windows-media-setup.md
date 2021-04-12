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
# <a name="detecting-setup-status-for-windows-media-setup"></a>Detectando o status da instalação da instalação do Windows Media

O código a seguir pode ser usado com os pacotes de redistribuição do Windows Media Player. O status da instalação é armazenado na entrada do registro **InstallResult** sob a seguinte subchave:

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ instalação**

A entrada do registro **InstallResult** tem o seguinte formato.



| Nome              | Tipo           | Valor                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Um **HRESULT** que indica se a instalação do Windows Media Player foi bem-sucedida e se uma reinicialização é necessária. |



 

Este é um código C++ de exemplo que pode ser incorporado a um aplicativo de instalação de chamada. Esse código irá definir as `fSuccess` `fRebootNeeded` variáveis e como **true** ou **false**, conforme apropriado, com base no valor **HRESULT** gravado pela instalação do Windows Media Player no pacote de redistribuição de componentes.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo o software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




