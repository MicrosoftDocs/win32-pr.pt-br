---
description: Representa o segmento de registro de arquivo. Este é o cabeçalho de cada segmento de registro de arquivo na MFT (tabela de arquivos mestre).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Estrutura de FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163918"
---
# <a name="file_record_segment_header-structure"></a>\_Estrutura do \_ cabeçalho do segmento de registro de arquivo \_

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

Representa o segmento de registro de arquivo. Este é o cabeçalho de cada segmento de registro de arquivo na MFT (tabela de arquivos mestre).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**MultiSectorHeader**
</dt> <dd>

O cabeçalho de multisetor definido pelo Gerenciador de cache. A estrutura de [**\_ \_ cabeçalho de vários setores**](multi-sector-header.md) sempre contém a assinatura "File" e uma descrição do local e do tamanho da matriz de sequência de atualização.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

O número de sequência. Esse valor é incrementado toda vez que um segmento de registro de arquivo é liberado; será 0 se o segmento não for usado. O campo **SequenceNumber** de uma referência de arquivo deve corresponder ao conteúdo desse campo; Se eles não corresponderem, a referência do arquivo estará incorreta e provavelmente será obsoleta.

</dd> <dt>

**Reserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

O deslocamento do primeiro registro de atributo, em bytes.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Os sinalizadores de arquivo.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>Do **arquivo \_ \_Segmento \_ de registro em \_ uso** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>Do **arquivo \_ Índice de nome de arquivo \_ \_ \_ presente** (0x0002)
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

Reservado.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Uma referência de arquivo para o segmento de registro de arquivo base para este arquivo. Se esse for o registro de arquivo base, o valor será 0. Consulte [**\_ \_ referência de segmento de MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved4**
</dt> <dd>

Reservado.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

A matriz de sequência de atualização para proteger as transferências de multisetor do segmento de registro de arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
