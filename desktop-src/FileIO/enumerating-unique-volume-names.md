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
# <a name="enumerating-volume-guid-paths"></a>Enumerando caminhos de GUID de volume

O exemplo de código neste tópico mostra como obter um caminho de **GUID** de volume para cada volume local associado a uma letra de unidade que está atualmente em uso no computador.

O exemplo de código usa a função [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .


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



Para obter um exemplo que enumera todos os volumes anexados localmente e exibe o caminho do dispositivo, o caminho do **GUID** do volume e os caminhos montados (incluindo as letras da unidade), consulte [exibindo caminhos de volume](displaying-volume-paths.md).

 

 



