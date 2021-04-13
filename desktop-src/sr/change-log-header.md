---
title: Estrutura de CHANGE_LOG_HEADER
description: O cabeçalho do log de alterações.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Restauração do sistema de estrutura CHANGE_LOG_HEADER
- Restauração do sistema de ponteiro de estrutura de PCHANGE_LOG_HEADER
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369284"
---
# <a name="change_log_header-structure"></a>ALTERAR \_ a \_ estrutura do cabeçalho do log

\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]

O cabeçalho do log de alterações.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**RecordHeader**
</dt> <dd>

Uma estrutura de [**\_ cabeçalho de registro**](record-header.md) . O membro **dwRecordType** deve ser definido como RecordTypeLogHeader (0). O membro **dwRecordSize** deve considerar todos os membros, mais o valor **DWORD** extra que segue esse cabeçalho. Para obter mais informações, consulte Comentários.

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Esse membro deve ser definido como 0xabcdef12.

</dd> <dt>

**dwLogVersion**
</dt> <dd>

Esse membro deve ser definido como 2.

</dd> <dt>

**Dataheader**
</dt> <dd>

Uma estrutura de [**\_ cabeçalho de registro**](record-header.md) . O membro **dwRecordType** deve ser definido como **RecordTypeVolumePath** (2).

</dd> <dt>

**byteData**
</dt> <dd>

O início de uma cadeia de caracteres terminada em nulo que especifica o caminho do volume.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse cabeçalho é seguido por um valor **DWORD** que deve ser idêntico ao valor do membro **dwRecordSize** de **RecordHeader**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                       |



 

 





