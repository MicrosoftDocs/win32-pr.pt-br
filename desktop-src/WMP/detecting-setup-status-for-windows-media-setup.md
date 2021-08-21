---
title: Detectando o status de instalação para Windows de mídia
description: Detectando o status de instalação para Windows de mídia
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player, detectando o status da instalação
- Windows Media Player, status da instalação
- Windows Media Player, redistribuindo software
- Windows Media Player,redistribuição de software
- detectando o status da instalação
- status da instalação
- redistribuindo software
- redistribuição de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797c7cb5fe4d34895109777c4da7e15489a0d32acd9cf42660b3346521f6f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340895"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Detectando o status de instalação para Windows de mídia

O código a seguir pode ser usado com os Windows Media Player pacotes de redistribuição. O status da instalação é armazenado na entrada do Registro **InstallResult** na seguinte sub-chave:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Setup**

A **entrada do Registro InstallResult** tem o seguinte formulário.



| Nome              | Tipo           | Valor                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Um **HRESULT que** indica se a Windows Media Player foi bem-sucedida e se uma reinicialização é necessária. |



 

Aqui está um código C++ de exemplo que pode ser incorporado em um aplicativo de configuração de chamada. Esse código definirá as variáveis e como true ou false, conforme apropriado, com base no valor HRESULT escrito por Windows Media Player Instalação no `fSuccess` `fRebootNeeded` pacote de redistribuição de componente.   


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

[**Redistribuindo Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




