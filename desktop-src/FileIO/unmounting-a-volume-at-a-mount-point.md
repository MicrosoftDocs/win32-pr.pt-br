---
description: Como excluir uma pasta montada usando a função DeleteVolumeMountPoint.
ms.assetid: 33049110-acf8-4db5-a9c4-bd4a884c8590
title: Excluindo uma pasta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b177aa2010d33b84aa98993d66952c50acb014e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502061"
---
# <a name="deleting-a-mounted-folder"></a>Excluindo uma pasta montada

O exemplo de código neste tópico mostra como excluir uma pasta montada usando a função [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) . Para obter mais informações, consulte [criando pastas montadas](mounting-and-dismounting-a-volume.md).


```C++
#define _WIN32_WINNT 0x0501

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void
Syntax (TCHAR *argv)
{
   _tprintf(TEXT("%s unmounts a volume from a volume mount point\n"), 
          argv);
   _tprintf(TEXT("For example: \"%s c:\\mnt\\fdrive\\\"\n"), argv);
}

int _tmain(int argc, TCHAR *argv[])
{
   BOOL bFlag;

   if (argc != 2)
   {
      Syntax (argv[0]);
      return (-1);
   }

// We should do some error checking on the path argument, such as
// ensuring that there is a trailing backslash.

   bFlag = DeleteVolumeMountPoint(
              argv[1] // Path of the volume mount point
           );

   _tprintf(TEXT("\n%s %s in unmounting the volume at %s\n"), argv[0],
           bFlag ? TEXT("succeeded") : TEXT("failed"), argv[1]);

   return (bFlag);
}
```



 

 



