---
description: Como retornar registros de diário de alterações que atendam aos critérios especificados.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Movimentação de um buffer de registros de diário de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755120"
---
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="ea2f9-103">Movimentação de um buffer de registros de diário de alterações</span><span class="sxs-lookup"><span data-stu-id="ea2f9-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="ea2f9-104">Os códigos de controle que retornam os registros do diário de alteração do USN (número de sequência de atualização), [**fsctl \_ ler o \_ \_ diário USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e [**\_ \_ \_ os dados USN de enumeração fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), retornam dados semelhantes no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="ea2f9-105">Ambos retornam um USN seguido por zero ou mais registros de diário de alterações, cada um em um [**\_ registro USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou estrutura [**\_ \_ v3 de registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .</span><span class="sxs-lookup"><span data-stu-id="ea2f9-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="ea2f9-106">O volume de destino para as operações de USN deve ser ReFS ou NTFS 3,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="ea2f9-107">Para obter a versão NTFS de um volume, abra um prompt de comando com direitos de acesso de administrador e execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ea2f9-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="ea2f9-108">**FSUtil.exe FSInfo NTFSInfo** \*X \*\* \* *:*</span><span class="sxs-lookup"><span data-stu-id="ea2f9-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="ea2f9-109">em que *X* é a letra da unidade do volume.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="ea2f9-110">A lista a seguir identifica maneiras de obter registros de diário de alterações:</span><span class="sxs-lookup"><span data-stu-id="ea2f9-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="ea2f9-111">Use [**os \_ \_ \_ dados USN de enumeração fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) para obter uma listagem (Enumeração) de todos os registros de diário de alterações entre dois USNs.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="ea2f9-112">Use [**fsctl \_ ler \_ \_ diário USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ser mais seletivo, como selecionar motivos específicos para alterações ou retornar quando um arquivo for fechado.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="ea2f9-113">Ambas as operações retornam apenas o subconjunto de registros de diário de alterações que atendem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="ea2f9-114">O USN retornado como o primeiro item no buffer de saída é o USN do próximo número de registro a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="ea2f9-115">Use esse valor para continuar lendo registros do limite final para frente.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="ea2f9-116">O membro **filename** do [**\_ registro USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou [**do \_ registro USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contém o nome do arquivo ao qual o registro em questão se aplica.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="ea2f9-117">O nome do arquivo varia em comprimento, portanto o **\_ registro USN \_ v2** e o **\_ registro USN \_ v3** são estruturas de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="ea2f9-118">Seu primeiro membro, **RecordLength**, é o comprimento da estrutura (incluindo o nome do arquivo), em bytes.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="ea2f9-119">Quando você trabalha com o membro **filename** do [**\_ registro USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e as estruturas do [**\_ registro USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , não presuma que o nome do arquivo contenha um \\ delimitador ' 0 ' à direita.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="ea2f9-120">Para determinar o comprimento do nome do arquivo, use o membro **FileNameLength** .</span><span class="sxs-lookup"><span data-stu-id="ea2f9-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="ea2f9-121">O exemplo a seguir [**chama \_ fsctl \_ ler \_ diário de USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e percorre o buffer dos registros de diário de alterações que a operação retorna.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



<span data-ttu-id="ea2f9-122">O tamanho em bytes de qualquer registro especificado por uma estrutura de registro [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou [**USN \_ registro \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) é no máximo `((MaxComponentLength - 1) * Width) + Size` onde *MaxComponentLength* é o comprimento máximo em caracteres do nome do arquivo de registro.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="ea2f9-123">A largura é o tamanho de um caractere largo e o tamanho *é o tamanho da* estrutura.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="ea2f9-124">Para obter o comprimento máximo, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine o valor apontado pelo parâmetro *lpMaximumComponentLength* .</span><span class="sxs-lookup"><span data-stu-id="ea2f9-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="ea2f9-125">Subtraia um de *MaxComponentLength* para considerar o fato de que a definição do [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e do [**\_ registro USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) inclui um caractere do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="ea2f9-126">Na linguagem de programação C, o maior tamanho de registro possível é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea2f9-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
