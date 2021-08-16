---
description: Representa um endereço na MFT (tabela de arquivos mestre). O endereço é marcado com um número de sequência reutilizado circularmente que é definido no momento em que a referência de segmento de MFT era válida.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Estrutura de MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0ef3ad4e727465b5ceb24c1ecc785f62b747da8113b8853bffc3431604089066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827082"
---
# <a name="mft_segment_reference-structure"></a>Estrutura de referência de \_ segmento de MFT \_

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

Representa um endereço na MFT (tabela de arquivos mestre). O endereço é marcado com um número de sequência reutilizado circularmente que é definido no momento em que a referência de segmento de MFT era válida.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>Membros

<dl> <dt>

**SegmentNumberLowPart**
</dt> <dd>

A parte inferior do número do segmento.

</dd> <dt>

**SegmentNumberHighPart**
</dt> <dd>

A parte superior do número do segmento.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

O número de sequência diferente de zero. O valor 0 é reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

O tipo de dados de **\_ referência de arquivo** é definido da seguinte maneira.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
