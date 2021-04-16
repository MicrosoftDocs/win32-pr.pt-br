---
description: Como obter um caminho de GUID de volume para cada volume local associado a uma letra de unidade que está atualmente em uso no computador.
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: Enumerando caminhos de GUID de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758351"
---
# <a name="enumerating-volume-guid-paths"></a><span data-ttu-id="72fd4-103">Enumerando caminhos de GUID de volume</span><span class="sxs-lookup"><span data-stu-id="72fd4-103">Enumerating Volume GUID Paths</span></span>

<span data-ttu-id="72fd4-104">O exemplo de código neste tópico mostra como obter um caminho de **GUID** de volume para cada volume local associado a uma letra de unidade que está atualmente em uso no computador.</span><span class="sxs-lookup"><span data-stu-id="72fd4-104">The code example in this topic shows you how to obtain a volume **GUID** path for each local volume associated with a drive letter that is currently in use on the computer.</span></span>

<span data-ttu-id="72fd4-105">O exemplo de código usa a função [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="72fd4-105">The code example uses the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



<span data-ttu-id="72fd4-106">Para obter um exemplo que enumera todos os volumes anexados localmente e exibe o caminho do dispositivo, o caminho do **GUID** do volume e os caminhos montados (incluindo as letras da unidade), consulte [exibindo caminhos de volume](displaying-volume-paths.md).</span><span class="sxs-lookup"><span data-stu-id="72fd4-106">For an example that enumerates all locally attached volumes and displays the device path, volume **GUID** path, and mounted paths (including drive letters), see [Displaying Volume Paths](displaying-volume-paths.md).</span></span>

 

 



