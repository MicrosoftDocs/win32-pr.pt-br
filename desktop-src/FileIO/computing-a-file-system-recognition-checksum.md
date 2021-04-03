---
description: A estrutura da estrutura de reconhecimento do sistema de arquivos \_ \_ \_ , definida internamente pelo Windows e usada pelo FRS (reconhecimento do sistema de arquivos), contém um valor de soma de verificação que deve ser computado corretamente para que o FRS funcione corretamente com um sistema de arquivos não reconhecido especificado.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calculando uma soma de verificação de reconhecimento do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922915"
---
# <a name="computing-a-file-system-recognition-checksum"></a><span data-ttu-id="9eb8a-103">Calculando uma soma de verificação de reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="9eb8a-103">Computing a File System Recognition Checksum</span></span>

<span data-ttu-id="9eb8a-104">A estrutura da estrutura de reconhecimento do sistema de arquivos, definida internamente pelo Windows e usada pelo FRS ( [reconhecimento do sistema de arquivos](file-system-recognition.md) ), contém um valor de soma de verificação que deve ser computado corretamente para que o FRS funcione corretamente com um sistema de arquivos não reconhecido especificado. [**\_ \_ \_**](file-system-recognition-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9eb8a-104">The [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) structure, defined internally by Windows and used by [file system recognition](file-system-recognition.md) (FRS), contains a checksum value that must be properly computed for FRS to work properly with a specified unrecognized file system.</span></span> <span data-ttu-id="9eb8a-105">O exemplo a seguir realiza esse cálculo.</span><span class="sxs-lookup"><span data-stu-id="9eb8a-105">The following example accomplishes this computation.</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a><span data-ttu-id="9eb8a-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9eb8a-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eb8a-107">Reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="9eb8a-107">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="9eb8a-108">**\_estrutura de \_ reconhecimento do sistema de arquivos \_**</span><span class="sxs-lookup"><span data-stu-id="9eb8a-108">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> </dl>

 

 



