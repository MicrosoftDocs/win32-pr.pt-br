---
description: Armazena informações sobre seções de memória compartilhada.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: SHAREDMEMORY_HEADER estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae596819feb4bd70aa47e7881521e5a69e5bd0a509b974e591d08907efda51c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966795"
---
# <a name="sharedmemory_header-structure"></a>Estrutura DE HEADER SHAREDMEMORY \_

Armazena informações sobre seções de memória compartilhada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbTotal**
</dt> <dd>

O tamanho, em bytes, dos dados referenciados por essa estrutura de header.

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

O tamanho, em bytes, de que os números de série são deslocamentos da estrutura do header.

</dd> <dt>

**idxEvent**
</dt> <dd>

O índice de evento. Esse valor é incrementado com eventos sucessivos.

</dd> <dt>

**dwEvent**
</dt> <dd>

O evento associado a este header.

</dd> <dt>

**Cid**
</dt> <dd>

O identificador de cursor referenciado pelo header de memória compartilhada.

</dd> <dt>

**sn**
</dt> <dd>

O número de série para o header de memória compartilhada.

</dd> <dt>

**sysEvt**
</dt> <dd>

O evento do sistema, ES \_ \* , associado a esse título. Consulte a seção de comentários para obter mais informações.

</dd> <dt>

**sysEvtData**
</dt> <dd>

A [**estrutura SYSTEM EVENT \_ \_ DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associada ao evento do sistema.

</dd> <dt>

**cPackets**
</dt> <dd>

Uma contagem dos pacotes associados à seção de memória compartilhada atual.

</dd> <dt>

**cbPackets**
</dt> <dd>

O tamanho, em bytes, dos pacotes associados à seção de memória compartilhada atual.

</dd> <dt>

**fSnsPresent**
</dt> <dd>

Um sinalizador que indica se os números de série estão presentes na seção de memória compartilhada atual.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores a seguir são definidos para **o membro sysEvt.**


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DADOS DE \_ EVENTO DO \_ SISTEMA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



