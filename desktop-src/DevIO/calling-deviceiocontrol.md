---
description: Chamando DeviceIoControl
ms.assetid: b4dbda89-effb-43f7-b3cc-774db57862a9
title: Chamando DeviceIoControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1372adc551d7816c047823b70a7541fa50318632ff7ea593f70896ceffc4f80c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642086"
---
# <a name="calling-deviceiocontrol"></a>Chamando DeviceIoControl

Um aplicativo pode usar a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para executar operações diretas de entrada e saída em ou recuperar informações sobre uma unidade de disquete, unidade de disco rígido, unidade de fita ou unidade CD-ROM. Para ver uma lista de códigos de controle padrão incluídos na documentação do SDK, consulte a seção Comentários de **DeviceIoControl.**

O exemplo a seguir demonstra como recuperar informações sobre a primeira unidade física no sistema. Ele usa a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para recuperar a alça do dispositivo para a primeira unidade física e, em seguida, usa [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com o código de controle [IOCTL \_ DISK GET DRIVE \_ \_ \_ GEOMETRY](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry) para preencher uma estrutura [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) de DISCO com informações sobre a unidade.


```C++
#define UNICODE 1
#define _UNICODE 1

/* The code of interest is in the subroutine GetDriveGeometry. The 
   code in main shows how to interpret the results of the call. */

#include <windows.h>
#include <winioctl.h>
#include <stdio.h>

#define wszDrive L"\\\\.\\PhysicalDrive0"

BOOL GetDriveGeometry(LPWSTR wszPath, DISK_GEOMETRY *pdg)
{
  HANDLE hDevice = INVALID_HANDLE_VALUE;  // handle to the drive to be examined 
  BOOL bResult   = FALSE;                 // results flag
  DWORD junk     = 0;                     // discard results

  hDevice = CreateFileW(wszPath,          // drive to open
                        0,                // no access to the drive
                        FILE_SHARE_READ | // share mode
                        FILE_SHARE_WRITE, 
                        NULL,             // default security attributes
                        OPEN_EXISTING,    // disposition
                        0,                // file attributes
                        NULL);            // do not copy file attributes

  if (hDevice == INVALID_HANDLE_VALUE)    // cannot open the drive
  {
    return (FALSE);
  }

  bResult = DeviceIoControl(hDevice,                       // device to be queried
                            IOCTL_DISK_GET_DRIVE_GEOMETRY, // operation to perform
                            NULL, 0,                       // no input buffer
                            pdg, sizeof(*pdg),            // output buffer
                            &junk,                         // # bytes returned
                            (LPOVERLAPPED) NULL);          // synchronous I/O

  CloseHandle(hDevice);

  return (bResult);
}

int wmain(int argc, wchar_t *argv[])
{
  DISK_GEOMETRY pdg = { 0 }; // disk drive geometry structure
  BOOL bResult = FALSE;      // generic results flag
  ULONGLONG DiskSize = 0;    // size of the drive, in bytes

  bResult = GetDriveGeometry (wszDrive, &pdg);

  if (bResult) 
  {
    wprintf(L"Drive path      = %ws\n",   wszDrive);
    wprintf(L"Cylinders       = %I64d\n", pdg.Cylinders);
    wprintf(L"Tracks/cylinder = %ld\n",   (ULONG) pdg.TracksPerCylinder);
    wprintf(L"Sectors/track   = %ld\n",   (ULONG) pdg.SectorsPerTrack);
    wprintf(L"Bytes/sector    = %ld\n",   (ULONG) pdg.BytesPerSector);

    DiskSize = pdg.Cylinders.QuadPart * (ULONG)pdg.TracksPerCylinder *
               (ULONG)pdg.SectorsPerTrack * (ULONG)pdg.BytesPerSector;
    wprintf(L"Disk size       = %I64d (Bytes)\n"
            L"                = %.2f (Gb)\n", 
            DiskSize, (double) DiskSize / (1024 * 1024 * 1024));
  } 
  else 
  {
    wprintf (L"GetDriveGeometry failed. Error %ld.\n", GetLastError ());
  }

  return ((int)bResult);
}
```



 

 
