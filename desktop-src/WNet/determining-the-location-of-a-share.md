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
# <a name="determining-the-location-of-a-share"></a><span data-ttu-id="cd681-103">Determinando o local de um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="cd681-103">Determining the Location of a Share</span></span>

<span data-ttu-id="cd681-104">O exemplo a seguir demonstra como chamar a função [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) para determinar o local de um compartilhamento em uma unidade redirecionada.</span><span class="sxs-lookup"><span data-stu-id="cd681-104">The following example demonstrates how to call the [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) function to determine the location of a share on a redirected drive.</span></span>

<span data-ttu-id="cd681-105">Primeiro, o exemplo de código chama a função **WNetGetUniversalName** , especificando o nível de informação de informações de [**\_ nome \_ Universal**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) para recuperar um ponteiro para uma cadeia de caracteres de nome UNC (Convenção de nomenclatura universal) para o recurso.</span><span class="sxs-lookup"><span data-stu-id="cd681-105">First the code sample calls the **WNetGetUniversalName** function, specifying the [**UNIVERSAL\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) information level to retrieve a pointer to a Universal Naming Convention (UNC) name string for the resource.</span></span> <span data-ttu-id="cd681-106">Em seguida, o exemplo chama **WNetGetUniversalName** uma segunda vez, especificando o nível de informações de informações de [**\_ nome \_ remoto**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) para recuperar duas cadeias de caracteres de informações de conexão de rede adicionais.</span><span class="sxs-lookup"><span data-stu-id="cd681-106">Then the sample calls **WNetGetUniversalName** a second time, specifying the [**REMOTE\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) information level to retrieve two additional network connection information strings.</span></span> <span data-ttu-id="cd681-107">Se as chamadas forem bem-sucedidas, o exemplo imprime o local do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="cd681-107">If the calls are successful, the sample prints the location of the share.</span></span>

<span data-ttu-id="cd681-108">Para testar o exemplo de código a seguir, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="cd681-108">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="cd681-109">Nomeie o código de exemplo GetUni. cpp.</span><span class="sxs-lookup"><span data-stu-id="cd681-109">Name the code sample GetUni.cpp.</span></span>
2.  <span data-ttu-id="cd681-110">Adicione o exemplo a um aplicativo de console chamado GetUni.</span><span class="sxs-lookup"><span data-stu-id="cd681-110">Add the sample to a console application called GetUni.</span></span>
3.  <span data-ttu-id="cd681-111">Vincule as bibliotecas shell32. lib, MPR. lib e NetApi32. lib à lista de bibliotecas do compilador.</span><span class="sxs-lookup"><span data-stu-id="cd681-111">Link the libraries Shell32.lib, Mpr.lib, and NetApi32.lib to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="cd681-112">No prompt de comando, altere para o diretório GetUni.</span><span class="sxs-lookup"><span data-stu-id="cd681-112">From the command prompt, change to the GetUni directory.</span></span>
5.  <span data-ttu-id="cd681-113">Compile GetUni. cpp.</span><span class="sxs-lookup"><span data-stu-id="cd681-113">Compile GetUni.cpp.</span></span>
6.  <span data-ttu-id="cd681-114">Execute o arquivo GetUni.exe seguido por uma letra de unidade e dois-pontos, desta forma:</span><span class="sxs-lookup"><span data-stu-id="cd681-114">Run the file GetUni.exe followed by a drive letter and colon, like this:</span></span>

    <span data-ttu-id="cd681-115">**GetUni H:\\**</span><span class="sxs-lookup"><span data-stu-id="cd681-115">**GetUni H:\\**</span></span>


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



 

 