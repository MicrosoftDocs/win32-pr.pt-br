---
description: Armazena informações sobre as seções de memória compartilhada.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Estrutura de SHAREDMEMORY_HEADER
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
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775647"
---
# <a name="sharedmemory_header-structure"></a>\_Estrutura de cabeçalho SHAREDMEMORY

Armazena informações sobre as seções de memória compartilhada.

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

O tamanho, em bytes, dos dados referenciados por essa estrutura de cabeçalho.

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

O tamanho, em bytes, que os números de série são deslocados da estrutura de cabeçalho.

</dd> <dt>

**idxEvent**
</dt> <dd>

O índice de eventos. Esse valor é incrementado com eventos sucessivos.

</dd> <dt>

**dwEvent**
</dt> <dd>

O evento associado a este cabeçalho.

</dd> <dt>

**CID**
</dt> <dd>

O identificador de cursor referenciado pelo cabeçalho da memória compartilhada.

</dd> <dt>

**sn**
</dt> <dd>

O número de série do cabeçalho da memória compartilhada.

</dd> <dt>

**sysEvt**
</dt> <dd>

O evento do sistema, prefixado SE \_ \* , associado a esse cabeçalho. Consulte a seção de comentários para obter mais informações.

</dd> <dt>

**sysEvtData**
</dt> <dd>

A estrutura de [**\_ \_ dados de evento do sistema**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associada ao evento do sistema.

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

Os valores a seguir são definidos para o membro **sysEvt** .


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

[**\_dados de evento do sistema \_**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



