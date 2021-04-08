---
description: Contém as informações de reconhecimento do sistema de arquivos em disco armazenadas no setor de inicialização de volumes (setor de disco lógico zero).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: Estrutura de FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010781"
---
# <a name="file_system_recognition_structure-structure"></a>\_Estrutura da \_ estrutura de reconhecimento do sistema de arquivos \_

Contém as informações de reconhecimento do sistema de arquivos em disco armazenadas no setor de inicialização do volume (setor de disco lógico zero).

Esta é uma estrutura de dados definida internamente não disponível em um cabeçalho público e é fornecida aqui para desenvolvedores de sistema de arquivos que desejam aproveitar o reconhecimento do sistema de arquivos. Para obter mais informações, consulte [reconhecimento do sistema de arquivos](file-system-recognition.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a>Membros

<dl> <dt>

**JMP**
</dt> <dd>

A instrução JMP. Esse membro de dados não está incluído no valor contido no membro de dados de **soma de verificação** .

</dd> <dt>

**FsName**
</dt> <dd>

O nome do sistema de arquivos. Essa é uma sequência de 8 caracteres ASCII que representa o nome legível não localizável do sistema de arquivos com o qual o volume é formatado.

Essa cadeia de caracteres está no mesmo local que o nome do sistema de arquivos OEM em um disco com uma estrutura de bloco de parâmetros do BIOS (BPB) normal.

</dd> <dt>

**MustBeZero**
</dt> <dd>

Espaço reservado que contém todos os zeros.

Esse membro de dados se sobrepõe ao que normalmente são os seguintes membros de dados em um BPB:

-   **BytesPerSector**
-   **SectorsPerCluster**
-   **ReservedSectorCount**

Como esses membros de dados são definidos como zero, isso deve ser suficiente para fazer com que o OSs anterior conclua que esse não é um BPB válido e, portanto, reconhece o volume.

</dd> <dt>

**Identificador**
</dt> <dd>

Identificador de estrutura. Deve conter o valor 0x53525346 organizado em ordem de byte little-endian.

Neste ponto da estrutura, os dados são alinhados a 16 bytes.

</dd> <dt>

**Comprimento**
</dt> <dd>

O número de bytes nessa estrutura, desde o início até o fim, incluindo o membro de dados **JMP** .

</dd> <dt>

**Soma**
</dt> <dd>

Uma soma de verificação de dois bytes calculada sobre os bytes começando no membro de dados **FsName** e terminando no último byte dessa estrutura, excluindo os membros de dados **JMP** e **checksum** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Calculando uma soma de verificação de reconhecimento do sistema de arquivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Reconhecimento do sistema de arquivos](file-system-recognition.md)
</dt> <dt>

[**\_informações de \_ reconhecimento do sistema de arquivos \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**\_reconhecimento do \_ sistema de arquivos de consulta fsctl \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

