---
description: Como retornar registros de diário de alterações que atendam aos critérios especificados.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Movimentação de um buffer de registros de diário de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9242d671cedfb5c9ef2b5fa836e29c455d09a9e1287b1ed035712f49c6c7d627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830146"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Movimentação de um buffer de registros de diário de alterações

Os códigos de controle que retornam os registros do diário de alteração do USN (número de sequência de atualização), [**fsctl \_ ler o \_ \_ diário USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e [**\_ \_ \_ os dados USN de enumeração fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), retornam dados semelhantes no buffer de saída. Ambos retornam um USN seguido por zero ou mais registros de diário de alterações, cada um em um [**\_ registro USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou estrutura [**\_ \_ v3 de registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .

O volume de destino para as operações de USN deve ser ReFS ou NTFS 3,0 ou posterior. Para obter a versão NTFS de um volume, abra um prompt de comando com direitos de acesso de administrador e execute o seguinte comando:

**FSUtil.exe FSInfo NTFSInfo** *X ** * *:*

em que *X* é a letra da unidade do volume.

A lista a seguir identifica maneiras de obter registros de diário de alterações:

-   Use [**os \_ \_ \_ dados USN de enumeração fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) para obter uma listagem (Enumeração) de todos os registros de diário de alterações entre dois USNs.
-   Use [**fsctl \_ ler \_ \_ diário USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ser mais seletivo, como selecionar motivos específicos para alterações ou retornar quando um arquivo for fechado.

> [!Note]  
> Ambas as operações retornam apenas o subconjunto de registros de diário de alterações que atendem aos critérios especificados.

 

O USN retornado como o primeiro item no buffer de saída é o USN do próximo número de registro a ser recuperado. Use esse valor para continuar lendo registros do limite final para frente.

O membro **filename** do [**\_ registro USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou [**do \_ registro USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contém o nome do arquivo ao qual o registro em questão se aplica. O nome do arquivo varia em comprimento, portanto o **\_ registro USN \_ v2** e o **\_ registro USN \_ v3** são estruturas de comprimento variável. Seu primeiro membro, **RecordLength**, é o comprimento da estrutura (incluindo o nome do arquivo), em bytes.

Quando você trabalha com o membro **filename** do [**\_ registro USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e as estruturas do [**\_ registro USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , não presuma que o nome do arquivo contenha um \\ delimitador ' 0 ' à direita. Para determinar o comprimento do nome do arquivo, use o membro **FileNameLength** .

O exemplo a seguir [**chama \_ fsctl \_ ler \_ diário de USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e percorre o buffer dos registros de diário de alterações que a operação retorna.


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



O tamanho em bytes de qualquer registro especificado por uma estrutura de registro [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou [**USN \_ registro \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) é no máximo `((MaxComponentLength - 1) * Width) + Size` onde *MaxComponentLength* é o comprimento máximo em caracteres do nome do arquivo de registro. A largura é o tamanho de um caractere largo e o tamanho *é o tamanho da* estrutura.

Para obter o comprimento máximo, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine o valor apontado pelo parâmetro *lpMaximumComponentLength* . Subtraia um de *MaxComponentLength* para considerar o fato de que a definição do [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e do [**\_ registro USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) inclui um caractere do nome do arquivo.

Na linguagem de programação C, o maior tamanho de registro possível é o seguinte:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
