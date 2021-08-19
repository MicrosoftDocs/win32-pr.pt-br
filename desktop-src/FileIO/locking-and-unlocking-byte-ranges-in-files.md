---
description: Código de exemplo que mostra o bloqueio de intervalo de bytes e o desbloqueio usando as funções LockFileEx e UnlockFileEx.
ms.assetid: 9d54fe11-b1ad-4723-a42a-00bc6dc64072
title: Bloqueio e desbloqueio de intervalos de bytes em arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ccd18fc8a5e2f143cb58717f72abbc135421ee802ff93b651dad0916ed8a953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951155"
---
# <a name="locking-and-unlocking-byte-ranges-in-files"></a>Bloqueio e desbloqueio de intervalos de bytes em arquivos

Embora o sistema permita que mais de um aplicativo Abra um arquivo e grave-o, os aplicativos não devem gravar sobre o trabalho de cada um deles. Um aplicativo pode evitar esse problema bloqueando temporariamente um intervalo de bytes em um arquivo.

As funções [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) e [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) bloqueiam um intervalo especificado de bytes em um arquivo. O intervalo pode se estender além da extremidade atual do arquivo. Bloquear parte de um arquivo dá aos threads do bloqueio acesso exclusivo ao intervalo de bytes especificado usando o identificador de arquivo especificado. As tentativas de acessar um intervalo de bytes bloqueado por outro processo sempre falham. Se o processo de bloqueio tentar acessar um intervalo de bytes bloqueado por meio de um segundo identificador de arquivo, a tentativa falhará.

> [!Note]  
> Não há suporte para arquivos mapeados de memória com bloqueios de intervalo de bytes.

 

A função [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) permite que um aplicativo especifique um dos dois tipos de bloqueios. Um *bloqueio exclusivo* nega a todos os outros processos acesso de leitura e gravação ao intervalo de bytes especificado de um arquivo. Um *bloqueio compartilhado* nega a todos os processos acesso de gravação ao intervalo de bytes especificado de um arquivo, incluindo o processo que primeiro bloqueia o intervalo de bytes. Isso pode ser usado para criar um intervalo de bytes somente leitura em um arquivo.

Um aplicativo desbloqueia o intervalo de bytes usando a função [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) ou [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) e deve desbloquear todas as áreas bloqueadas antes de fechar um arquivo.

Para obter um exemplo de como usar o [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile), consulte [acrescentar um arquivo a outro arquivo](appending-one-file-to-another-file.md).

Os exemplos a seguir mostram como usar [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex). O primeiro exemplo é uma demonstração simples para criar um arquivo, gravar alguns dados nele e bloquear uma seção no meio.

**Observação**  Este exemplo não altera os dados depois que o arquivo está bloqueado.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>

#define NUMWRITES 10
#define TESTSTRLEN 11

const char TestData[NUMWRITES][TESTSTRLEN] = 
{ 
    "TestData0\n",
    "TestData1\n",
    "TestData2\n",
    "TestData3\n",
    "TestData4\n",
    "TestData5\n",
    "TestData6\n",
    "TestData7\n",
    "TestData8\n",
    "TestData9\n"
};

int main(int argc, char *argv[])
{
    BOOL fSuccess = FALSE;

    // Create the file, open for both read and write.
    HANDLE hFile = CreateFile(TEXT("datafile.txt"),
                       GENERIC_READ | GENERIC_WRITE,
                       0,          // open with exclusive access
                       NULL,       // no security attributes
                       CREATE_NEW, // creating a new temp file
                       0,          // not overlapped index/O
                       NULL);
    
    if (hFile == INVALID_HANDLE_VALUE) 
    {
        // Handle the error.
        printf("CreateFile failed (%d)\n", GetLastError());
        return (1);
    }

    // Write some data to the file.
    DWORD dwNumBytesWritten = 0;

    for (int i=0; i<NUMWRITES; i++)
    {
        fSuccess = WriteFile(hFile,
                             TestData[i],
                             TESTSTRLEN,
                             &dwNumBytesWritten,
                             NULL);  // sync operation.
        if (!fSuccess) 
        {
           // Handle the error.
           printf("WriteFile failed (%d)\n", GetLastError());
           return (2);
        }
    } 

    FlushFileBuffers(hFile);

    // Lock the 4th write-section.  
    // First, set up the Overlapped structure with the file offset 
    // required by LockFileEx, three lines in to the file.
    OVERLAPPED sOverlapped;
    sOverlapped.Offset = TESTSTRLEN * 3;
    sOverlapped.OffsetHigh = 0;

    // Actually lock the file.  Specify exclusive access, and fail 
    // immediately if the lock cannot be obtained.
    fSuccess = LockFileEx(hFile,         // exclusive access, 
                          LOCKFILE_EXCLUSIVE_LOCK | 
                          LOCKFILE_FAIL_IMMEDIATELY,
                          0,             // reserved, must be zero
                          TESTSTRLEN,    // number of bytes to lock
                          0,
                          &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("LockFileEx failed (%d)\n", GetLastError());
       return (3);
    }
    else printf("LockFileEx succeeded\n");

    /////////////////////////////////////////////////////////////////
    // Add code that does something interesting to locked section,  /
    // which should be line 4                                       /
    /////////////////////////////////////////////////////////////////

    // Unlock the file.
    fSuccess = UnlockFileEx(hFile, 
                            0,             // reserved, must be zero
                            TESTSTRLEN,    // num. of bytes to unlock
                            0,
                            &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("UnlockFileEx failed (%d)\n", GetLastError());
       return (4);
    }
    else printf("UnlockFileEx succeeded\n");

    // Clean up handles, memory, and the created file.
    fSuccess = CloseHandle(hFile);
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("CloseHandle failed (%d)\n", GetLastError());
       return (5);
    }

    fSuccess = DeleteFile(TEXT("datafile.txt"));
    if (!fSuccess) 
    {
        // Handle the error.
       printf ("DeleteFile failed (%d)\n", GetLastError());
       return (6);
    }
    return (0);
}
```



O exemplo a seguir é uma demonstração avançada do bloqueio de intervalo de bytes, usando vários threads e um banco de dados simples executando operações aleatórias em um único arquivo de dados. Para obter mais informações, consulte os comentários de código inserido e a seção seguindo o código de exemplo.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#define UNICODE
#define _CRT_RAND_S
#include <stdlib.h>
#include <windows.h>

#include <stdio.h>

#include <malloc.h>
#include <conio.h>
#include <process.h>
#include <winioctl.h>

#define RECORD_SIZE 0x300
#define NUM_RECORDS 0x1000
#define NUM_THREADS 8

#define NUM_FILEOPS 500

#define BITMAP_SIZE ((NUM_RECORDS) / 8)
#define DATA_SIZE   ((RECORD_SIZE) - sizeof(RECORD_HEADER))

#define MSG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#if defined BRLS_DEBUG

#define DBG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#else

#define DBG_PRINTF(...)
#define PrintBitmap(...)

#endif


#define MASTER_RECORD_TYPE_CODE 'rtsM'
#define DATA_RECORD_TYPE_CODE   'ataD'


//
//  Record type definitions.
//
typedef struct _RECORD_HEADER {
    ULONG TypeCode;     // Either MASTER_RECORD_TYPE_CODE or DATA_RECORD_TYPE_CODE.
    ULONG SeqNumber;    // Starts at 1 and is incremented every time contents are modified.
} RECORD_HEADER;

typedef struct _MASTER_RECORD {
    RECORD_HEADER Header;
    BYTE Bitmap[BITMAP_SIZE];  // A bitmap indicating which records are allocated.
} MASTER_RECORD;

typedef struct _DATA_RECORD {
    RECORD_HEADER Header;
    BYTE Data[DATA_SIZE];       // Record raw data.
} DATA_RECORD;


//
//  Types of I/O for IoRecord.
//
typedef enum {
    IoRead,
    IoWrite,
    IoLock,
    IoUnlock
} IO_TYPE;


//
//  Types of operations for OperateOnRecord.
//
typedef enum {
    CreateRecord = 0,
    DeleteRecord,
    ModifyRecord,
    MaxOprRecord
} OPERATION;


//
//  Parameter block for I/Os passed to IoRecord.
//
typedef struct _IO_PARAM {
    IO_TYPE Type;
    union _IO_PARAM_PARAMS {
        struct {
            PVOID Data;
            ULONG RecSize;
        } IoInfo;
        struct {
            BOOL Exclusive;
        } LockInfo ;
    } Params;
} IO_PARAM, *PIO_PARAM;

void ErrorExitThread()
//
//  This function is called immediately after an unrecoverable error is logged.
//
{
    MSG_PRINTF(L"An error has been logged, calling ExitThread.\n");
    ExitThread(1);
}

BOOL IoRecord(HANDLE hFile, ULONG RecNumber, PIO_PARAM pIoParam)
//
//  This function performs I/O (read, write, lock or unlock) in a record, according
//  to the parameters passed in the IO_PARAM block.
//
//  Arguments:
//      hFile       - Handle to the file containing the records.
//      RecNumber   - Number of the record to be operated on.
//      pIoParam    - Pointer to IO_PARAM structure.
//
//  Return value:
//      TRUE if the I/O succeeded, FALSE if not.
//
{
    OVERLAPPED Overlapped;
    BOOL Result;
    ULARGE_INTEGER RecOffset;
    DWORD NumBytes;

    //  Initialize Overlapped.
    SecureZeroMemory(&Overlapped, sizeof(OVERLAPPED));
    Overlapped.hEvent = CreateEvent(NULL,
        FALSE,
        FALSE,
        NULL);

    if (NULL == Overlapped.hEvent) 
    {
        MSG_PRINTF(L"CreateEvent for Overlapped.hEvent failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Calculate record position.
    RecOffset.QuadPart = RecNumber * RECORD_SIZE;

    Overlapped.Offset     = RecOffset.LowPart;
    Overlapped.OffsetHigh = RecOffset.HighPart;

    //  Issue the operation.
    switch (pIoParam->Type) 
    {
    case IoLock:
        Result = LockFileEx(hFile,
            pIoParam->Params.LockInfo.Exclusive ? LOCKFILE_EXCLUSIVE_LOCK : 0,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoUnlock:
        Result = UnlockFileEx(hFile,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoRead:
        Result = ReadFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    case IoWrite:
        Result = WriteFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    default:
        Result = FALSE;
        break;
    }

    if (!Result) 
    {
        if (GetLastError() == ERROR_IO_PENDING) 
        {
            //  Wait until the operation finishes.
            if (GetOverlappedResult(hFile,
                &Overlapped,
                &NumBytes,
                TRUE) == FALSE) 
            {
                MSG_PRINTF(L"GetOverlappedResult for Overlapped.hEvent failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }
            Result = TRUE;
        } else {
            MSG_PRINTF(L"IoRecord failed with error 0x%08x. Failure passed to caller.\n", 
                GetLastError());
        }
    }
    CloseHandle(Overlapped.hEvent);
    return Result;
}


//
//  The following functions are wrappers around IoRecord, they just set the correct
//  parameters in the IO_PARAM block to correspond to the requested operation and
//  pass that to IoRecord.
//
BOOL ReadRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoRead;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL WriteRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoWrite;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL LockRecord(HANDLE hFile, ULONG RecNumber, BOOL Exclusive)
{
    IO_PARAM IoParam;

    IoParam.Type                      = IoLock;
    IoParam.Params.LockInfo.Exclusive = Exclusive;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL UnlockRecord(HANDLE hFile, ULONG RecNumber)
{
    IO_PARAM IoParam;

    IoParam.Type = IoUnlock;

    return IoRecord(hFile, RecNumber, &IoParam);
}


ULONG ReserveFirstFreeRecord(BYTE* Bitmap)
//
//  This function iterates through the bitmap and reserves the first free record
//  it can find in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//
//  Return value:
//      Either zero, if there are no free records, or the position of the record
//      that was just reserved.
//          
{
    int i;
    BYTE Bit = 1;

    for (i = 0; i < NUM_RECORDS; i++) 
    {
        if (Bitmap[i / 8] & Bit) 
        {
            Bit <<= 1;
            if (Bit == 0) { Bit = 1; }
        } else {
            Bitmap[i / 8] |= Bit;
            return i;
        }
    }

    return 0;
}


BOOL TestBit(BYTE* Bitmap, ULONG Bit)
//
//  This function tests if a given bit is set in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
//  Return value:
//      TRUE if the bit is set, FALSE otherwise.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    return (BOOL)(Bitmap[Byte] & (1 << Bit));
}


void ClearBit(BYTE* Bitmap, ULONG Bit)
//
//  This function clears a given bit in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    Bitmap[Byte] &= ~(1 << Bit);
}


#ifdef BRLS_DEBUG
void PrintBitmap(BYTE* Bitmap)
//
//   This function prints the whole bitmap, for debugging purposes.
//
//   Arguments:
//      Bitmap  - Pointer to the bitmap.
//
{
    int i;

    for (i = 0; i < BITMAP_SIZE; i++) 
    {
        wprintf(L"%1x", Bitmap[i]);
    }

    wprintf(L"\n");
}
#endif


void InitRecord(RECORD_HEADER* Record, BOOL Master, ULONG SeqNumber)
//
//  This function initializes a in-memory record structure with the correct
//  type code and sequence number. In case of the Master Record, the bitmap
//  is initialized too.
//
//  Arguments:
//      Record      - Pointer to the record structure.
//      Master      - TRUE if this is a Master Record, FALSE otherwise.
//      SeqNumber   - Initial sequence number.
//
{
    ULONG RecSize   = Master ? sizeof(MASTER_RECORD)   : sizeof(DATA_RECORD);
    ULONG TypeCode  = Master ? MASTER_RECORD_TYPE_CODE : DATA_RECORD_TYPE_CODE;

    SecureZeroMemory(Record, RecSize);

    Record->TypeCode  = TypeCode;
    Record->SeqNumber = Master ? 0 : SeqNumber;

    if (Master) 
    {
        ((MASTER_RECORD*)Record)->Bitmap[0] = 1;
    }
}


DATA_RECORD* PrepareRecord(ULONG SeqNumber)
//
//  This function allocates a new in-memory record structure and initializes it
//  as a brand new data record.
//
//  Arguments:
//      SeqNumber   - Sequence number with which to initialize the record.
//
//  Return value:
//      Pointer to the record structure.
//
{
    DATA_RECORD* Record = NULL;

    Record = (DATA_RECORD*) malloc(sizeof(DATA_RECORD));

    if (Record == NULL) 
    {
        MSG_PRINTF(L"Critical error: malloc for CreateRecord failed.\n");
        ErrorExitThread();
    }

    InitRecord((RECORD_HEADER*)Record, FALSE, SeqNumber);

    return Record;
}


void WriteData(DATA_RECORD* Record)
//
//  This function fills a in-memory data record structure with random data.
//  Errors do not interrupt execution.
//
//  Arguments:
//      Record  - Pointer to the record structure.
//
{
    PUINT iData;
    int i;
    errno_t err;

    iData = (PUINT)Record->Data;

    for (i = 0; i < DATA_SIZE; i += sizeof(ULONG), iData++) 
    {
        err = rand_s(iData);
        if (err != 0) 
        {
            MSG_PRINTF(L"rand_s for WriteData failed with error 0x%08x, continuing execution.\n", 
                err);
        }
    }
}


BOOL OperateOnRecord(HANDLE hFile, PULONG RecNumber, OPERATION Operation)
//
//  This function executes a high-level operation in a record (create, modify or delete).
//
//  Arguments:
//      hFile       - Handle to the file containing the record to be operated on.
//      RecNumber   - Pointer to a ULONG that either will receive the number of the
//                    record created by this operation or just contains the number
//                    of the record that will be modified or deleted.
//      Operation   - Operation to be performed (CreateRecord, ModifyRecord or
//                    DeleteRecord).
//
//  Return value:
//      TRUE if the operation succeeded, FALSE otherwise.
//
{
    BOOL Result;
    BOOL Exists;
    BOOL ExclusiveLock;
    MASTER_RECORD MasterRecord;
    DATA_RECORD*  Record;

    //  Fail operations on Master Record.
    if ((Operation != CreateRecord) && (*RecNumber == 0)) 
    {
        MSG_PRINTF(L"Cannot operate on Master Record.\n");
        return FALSE;
    }

    //  Lock Master Record. If we're just modifying a record, we can get a
    //  shared lock.
    ExclusiveLock = (Operation != ModifyRecord);

    Result = LockRecord(hFile, 0, ExclusiveLock);
    if (!Result) 
    {
        MSG_PRINTF(L"LockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Read in Master Record.
    Result = ReadRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
    if (!Result) 
    {
        MSG_PRINTF(L"ReadRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (MasterRecord.Header.TypeCode != MASTER_RECORD_TYPE_CODE) 
    {
        MSG_PRINTF(L"Master Record corruption error: wrong typecode!\n");
        ErrorExitThread();
    }

    DBG_PRINTF(L"MasterRecord bitmap (before): ");
    PrintBitmap(MasterRecord.Bitmap);

    if (Operation != CreateRecord) 
    {
        //  Test the bit in the bitmap corresponding to this record.
        Exists = TestBit(MasterRecord.Bitmap, *RecNumber);

        //  Clear the bit if we are deleting the record.
        if ((Operation == DeleteRecord) && Exists) 
        {
            ClearBit(MasterRecord.Bitmap, *RecNumber);
        }

    } else {

        //  Reserve the first free record.
        *RecNumber = ReserveFirstFreeRecord(MasterRecord.Bitmap);

        if (*RecNumber != 0) 
        {
            Exists = TRUE;
        } else {
            Exists = FALSE;
            MSG_PRINTF(L"File is full!\n");
        }
    }

    DBG_PRINTF(L"MasterRecord bitmap (after): ");
    PrintBitmap(MasterRecord.Bitmap);

    if ((Operation != ModifyRecord) && Exists) 
    {
        //  Update the Master Record's sequence number.
        MasterRecord.Header.SeqNumber++;

        //  Write Master Record down.
        Result = WriteRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord (MasterRecord) for CreateRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }
    }

    //  Unlock Master Record.
    Result = UnlockRecord(hFile, 0);
    if (!Result) 
    {
        MSG_PRINTF(L"UnlockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (!Exists) 
    {
        if (*RecNumber != 0) 
        {
            MSG_PRINTF(L"Record %d not present!\n", *RecNumber);
        }
        return FALSE;
    }

    //  For record deletion, processing is done and skip to write.
    //  Otherwise, there is more to do.
    if (Operation != DeleteRecord) 
    {
        //  Prepare a new record in memory.
        Record = PrepareRecord(1);

        //  Lock the record exclusively.
        Result = LockRecord(hFile, *RecNumber, TRUE);
        if (!Result) 
        {
            MSG_PRINTF(L"LockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        if (Operation == ModifyRecord) 
        {
            //  Read the record in from the file if we're modifying it.
            Result = ReadRecord(hFile, *RecNumber, Record, RECORD_SIZE);
            if (!Result) 
            {
                MSG_PRINTF(L"ReadRecord for ModifyRecord failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }

            //  Update record sequence number.
            Record->Header.SeqNumber++;
        }

        //  Write to the in-memory record.
        WriteData(Record);

        //  Write the record to the file.
        Result = WriteRecord(hFile, *RecNumber, Record, RECORD_SIZE);
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Unlock the record.
        Result = UnlockRecord(hFile, *RecNumber);
        if (!Result) 
        {
            MSG_PRINTF(L"UnlockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Free the record structure.
        free(Record);
    }

    return TRUE;
}


ULONG RandomOption(ULONG NumOpts)
//
//  This function returns a random number between 0 and (NumOpts - 1).
//  It basically is a random option select.
//
//  Arguments:
//      NumOpts - Number of options to choose from.
//
//  Return value:
//      A random option (random ULONG x | 0 <= x < NumOpts).
//
{
    UINT Random;
    errno_t err;

    err = rand_s(&Random);
    if (err != 0) 
    {
        MSG_PRINTF(L"rand_s for RandomOption failed with error 0x%08x\n", 
            err);
    }

    return Random % NumOpts;
}


DWORD WINAPI WorkerThread(PVOID data)
//
//  This is the tight loop executed by each of the threads operating in the file.
//  Each thread has its own handle to the same file. After obtaining that handle,
//  they go into a tight loop in which a record number and a record operation are
//  chosen at random and that operation is then performed in that record.
//
//  Arguments:
//      Data    - PVOID to a string containing the file name (so it can be opened).
//
//  Return value:
//      It should not return.
//
{
    HANDLE hFile;
    LPCWSTR FileName = (LPCWSTR)data;
    ULONG RecNumber;
    OPERATION Operation;
    BOOL Result;

    UINT i;

    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED,
        NULL);

    if (hFile == INVALID_HANDLE_VALUE) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Main loop for doing the random operations.
    for (i = 0; i < NUM_FILEOPS; i++) 
    {
        RecNumber = RandomOption(NUM_RECORDS);
        Operation = (OPERATION)RandomOption(MaxOprRecord);

        //  Output message as to what action is being attempted.
        switch (Operation) 
        {
        case CreateRecord:
            MSG_PRINTF(L"attempting record creation.\n");
            break;
        case ModifyRecord:
            MSG_PRINTF(L"attempting modification of record %d.\n", RecNumber);
            break;
        case DeleteRecord:
            MSG_PRINTF(L"attempting deletion of record %d.\n", RecNumber);
            break;
        }

        //  Perform the actual operation and handle the result, 
        //  then loop again until done.
        Result = OperateOnRecord(hFile, &RecNumber, Operation);

        if (Result) 
        {
            switch (Operation) 
            {
            case CreateRecord:
                MSG_PRINTF(L"created record %d.\n", RecNumber);
                break;

            case ModifyRecord:
                MSG_PRINTF(L"modified record %d.\n", RecNumber);
                break;

            case DeleteRecord:
                MSG_PRINTF(L"deleted record %d.\n", RecNumber);
                break;
            }
        }
    }

    CloseHandle(hFile);
    MSG_PRINTF(L"%d file operations complete. Exiting thread.\n", i);

    return 0;
}


BOOL InitNewFile(LPCWSTR FileName)
//
//  This function initializes a file with records. If the file already exists, it
//  just returns, assuming it has a valid Master Record on it. If it does not 
//  exist, a brand new file is created and initialized with a clean Master Record.
//
//  Arguments:
//      FileName    - Name of the file to be initialized.
//
//  Return value:
//      TRUE if the initialization succeeded, FALSE otherwise.
//      
{
    HANDLE hFile;
    MASTER_RECORD MasterRecord;
    DWORD BytesWritten;
    DWORD Result;

    //
    //  Create the file or open existing.
    //
    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_ALWAYS,
        FILE_ATTRIBUTE_NORMAL,
        NULL);

    if (INVALID_HANDLE_VALUE == hFile) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        return FALSE;
    } 
    else if (ERROR_ALREADY_EXISTS == GetLastError()) 
    {
        //  This is ok, simply assume it's a valid file.
        //  Note that this does not actually test that the file
        //  is valid for this application. That error is caught later.
        CloseHandle(hFile);
        return TRUE;
    } //  The implied "else" is that the handle is a good one.


    InitRecord((RECORD_HEADER*)&MasterRecord, TRUE, 0);

    Result = WriteFile(hFile,
        &MasterRecord,
        sizeof(MASTER_RECORD),
        &BytesWritten,
        NULL);

    if (!Result) 
    {
        MSG_PRINTF(L"WriteFile failed with error 0x%08x.\n", 
            GetLastError());
    }

    CloseHandle(hFile);

    return Result;
}


int __cdecl wmain(int argc, LPCWSTR argv[])
//
//  Main function. Reads file name from command line argument, initializes the file
//  and starts the worker threads, waiting for them to return.
//
{
    HANDLE gThread[NUM_THREADS];

    DWORD IdThread;
    DWORD ResultCode;
    LPCWSTR FileName = NULL;

    if (argc != 2) {
        wprintf(L"Invalid number of arguments!\n");
        wprintf(L"Usage: %ws file_name\n", argv[0]);
        return -1;
    }

    FileName = argv[1];

    if (!InitNewFile(FileName))
    {
        wprintf(L"Unable to initialize the data file %ws.\n", FileName);
    }

    wprintf(L"Main thread creating %d worker threads for processing.\n", 
        NUM_THREADS);
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        gThread[i] = CreateThread(NULL,
            0,
            (LPTHREAD_START_ROUTINE)WorkerThread,
            (PVOID)FileName,
            0,
            &IdThread);
    }

    wprintf(L"Main thread waiting for worker threads to exit...\n");

    ResultCode = WaitForMultipleObjects(
        NUM_THREADS,
        gThread,
        TRUE,
        INFINITE);

    wprintf(L"WaitForMultipleObjects returned 0x%08x, execution complete.\n",
        ResultCode);

    // Do some clean-up.
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        CloseHandle(gThread[i]);
    }

    return 0;
}
```



este exemplo é um aplicativo de console Windows que executa vários acessos simultâneos a um arquivo, todos coordenados por intervalos de intervalo de bytes usando um banco de dados simples, composto por vários registros de um tamanho fixo. Observe que true simultaneidade depende de quantos núcleos de processador existem no sistema host.

Todos os registros têm os dois primeiros campos em comum: um código de tipo e um número de sequência. O código de tipo é um dos dois códigos: o código "Mstr" refere-se ao tipo de **\_ registro mestre** e o código de "dados" refere-se a um tipo de **\_ registro de dados** . Pode haver apenas um **\_ registro mestre** e zero ou mais **\_ registros de dados** s. Para este exemplo, os dados contidos nos registros de dados são gerados aleatoriamente. O segundo campo, o número de sequência, é incrementado toda vez que um registro é modificado.

Quando a execução for iniciada, se o arquivo de dados ainda não existir, ele será criado e inicializado pela função **InitNewFile** . A função **InitNewFile** grava um registro do tipo Master com um bitmap vazio no início. Se o arquivo já existir, ele será aberto; Supõe-se que tenha um registro mestre válido no início.

Depois que o arquivo é criado com êxito ou aberto com êxito, vários threads de trabalho são iniciados e todos eles executam um loop no qual uma operação e um registro são escolhidos aleatoriamente e essa operação é tentada nesse registro. Como essas operações são aleatórias, nem todas elas são realizadas com sucesso, mas não são necessariamente erros. As informações de status apropriadas são registradas no console do.

As operações possíveis são as seguintes: criação de um novo registro, modificação de um registro existente ou exclusão de um registro existente. A operação de criação examina o bitmap para localizar o primeiro registro gratuito e aloca esse registro como o novo registro. A operação de modificação lê o bitmap para ver se o registro realmente existe e, em caso afirmativo, modifica esse registro. A operação de exclusão limpa o bit no bitmap correspondente ao registro, liberando o espaço que o registro ocupa para uma alocação futura. Além disso, essas operações são divididas em duas partes: acesso ao MasterRecord, onde os metadados são armazenados e acesso ao próprio registro de dados.

Como eles gravam dados nos registros de dados, a criação de registro e as operações de modificação de registro são as únicas que exigem acesso ao registro de dados. Por esse motivo, a região coberta pelo registro é bloqueada exclusivamente antes da operação ser executada. As operações de criação e exclusão modificam o bitmap, portanto, eles precisam bloquear o registro mestre exclusivamente. No entanto, as operações de modificação de registro só precisam ler o bitmap, não gravar nele, para verificar se o arquivo existe. Para essa operação, o registro mestre precisa apenas de um bloqueio de intervalo de bytes compartilhado.

Os bloqueios de intervalo de bytes exclusivos impedem o acesso de leitura e gravação de todos os outros identificadores para o arquivo, e esse é o motivo pelo qual eles são usados durante a gravação em um registro. Por outro lado, um bloqueio de intervalo de bytes compartilhado impede o acesso de gravação de todos os identificadores, incluindo o identificador que possui o bloqueio, mas permite o acesso de leitura de todos eles.

Para demonstrar o uso de bloqueios de intervalo de bytes com o arquivo, toda e/s neste exemplo, além da inicialização do novo arquivo, é feita por meio de um identificador de arquivo assíncrono. Isso pode ser visto na função **IoRecord** nos casos **IoLock** e **IoUnlock** dentro da instrução switch. As funções [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) e [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) são usadas com o modelo de e/s sobreposto, passando uma estrutura [**sobreposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) para eles com o deslocamento para o início do intervalo bloqueado e um evento que será sinalizado após o bloqueio desse intervalo ser concedido, a menos que a função retorne imediatamente.

Depois de emitir a solicitação de e/s assíncrona, a próxima operação na função **IoRecord** é aguardar a operação embutida. Isso geralmente é um cenário abaixo do ideal quando o desempenho máximo é desejado e é usado aqui para simplificar. Em aplicativos de produção, o uso de portas de conclusão de e [/s](i-o-completion-ports.md) ou mecanismos semelhantes é preferencial porque libera threads para realizar outro processamento enquanto a e/s é concluída.

O exemplo termina depois de executar as operações aleatórias **num \_ FILEOPS** . Cada thread registrará seu status de encerramento como uma condição de erro ou um encerramento normal. Observe que nem todos os threads terminarão ao mesmo tempo, dependendo de quantos núcleos de processador o sistema host tem e da velocidade do subsistema de e/s.

 

 



