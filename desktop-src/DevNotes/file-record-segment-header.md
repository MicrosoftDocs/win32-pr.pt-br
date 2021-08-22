---
description: Representa o segmento de registro de arquivo. Esse é o header para cada segmento de registro de arquivo na MFT (tabela de arquivos mestre).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: FILE_RECORD_SEGMENT_HEADER estrutura
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
ms.openlocfilehash: 0c9d7a3653ad965141e691546866f599d8615f5f12feb92fa25c861d7c429b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260596"
---
# <a name="file_record_segment_header-structure"></a>Estrutura DE \_ \_ HEADER DO \_ SEGMENTO DE REGISTRO DE ARQUIVO

\[Essa estrutura é válida somente para a versão 3 dos volumes NTFS; ele pode ser alterado em versões futuras.\]

Representa o segmento de registro de arquivo. Esse é o header para cada segmento de registro de arquivo na MFT (tabela de arquivos mestre).

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

O header multisector definido pelo gerenciador de cache. A [**estrutura MULTI SECTOR \_ \_ HEADER**](multi-sector-header.md) sempre contém a assinatura "FILE" e uma descrição do local e do tamanho da matriz de sequência de atualização.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

O número de sequência. Esse valor é incrementado sempre que um segmento de registro de arquivo é liberado; será 0 se o segmento não for usado. O **campo SequenceNumber** de uma referência de arquivo deve corresponder ao conteúdo desse campo; se eles não corresponderem, a referência de arquivo será incorreta e provavelmente obsoleta.

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

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**ARQUIVO \_ SEGMENTO \_ DE REGISTRO EM \_ \_ USO** (0X0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**ARQUIVO \_ FILE \_ NAME \_ INDEX \_ PRESENT** (0x0002)
</dt> </dl> </dd> <dt>

**Reservado3**
</dt> <dd>

Reservado.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Uma referência de arquivo para o segmento de registro de arquivo base para esse arquivo. Se esse for o registro de arquivo base, o valor será 0. Consulte [**REFERÊNCIA DE SEGMENTO \_ MFT \_**](mft-segment-reference.md).

</dd> <dt>

**Reservado4**
</dt> <dd>

Reservado.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

A matriz de sequência de atualização para proteger transferências multissetor do segmento de registro de arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de header associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e a versão secundária 0 ou 1, conforme relatado por [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
