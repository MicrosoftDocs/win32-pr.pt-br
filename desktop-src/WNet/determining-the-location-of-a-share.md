---
title: Determinando o local de um compartilhamento
description: O exemplo a seguir demonstra como chamar a função WNetGetUniversalName para determinar o local de um compartilhamento em uma unidade redirecionada.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917510"
---
# <a name="determining-the-location-of-a-share"></a>Determinando o local de um compartilhamento

O exemplo a seguir demonstra como chamar a função [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) para determinar o local de um compartilhamento em uma unidade redirecionada.

Primeiro, o exemplo de código chama a função **WNetGetUniversalName** , especificando o nível de informação de informações de [**\_ nome \_ Universal**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) para recuperar um ponteiro para uma cadeia de caracteres de nome UNC (Convenção de nomenclatura universal) para o recurso. Em seguida, o exemplo chama **WNetGetUniversalName** uma segunda vez, especificando o nível de informações de informações de [**\_ nome \_ remoto**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) para recuperar duas cadeias de caracteres de informações de conexão de rede adicionais. Se as chamadas forem bem-sucedidas, o exemplo imprime o local do compartilhamento.

Para testar o exemplo de código a seguir, execute as seguintes etapas:

1.  Nomeie o código de exemplo GetUni. cpp.
2.  Adicione o exemplo a um aplicativo de console chamado GetUni.
3.  Vincule as bibliotecas shell32. lib, MPR. lib e NetApi32. lib à lista de bibliotecas do compilador.
4.  No prompt de comando, altere para o diretório GetUni.
5.  Compile GetUni. cpp.
6.  Execute o arquivo GetUni.exe seguido por uma letra de unidade e dois-pontos, desta forma:

    **GetUni H:\\**


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 