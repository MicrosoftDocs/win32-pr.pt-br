---
description: Um quadro real do driver.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Estrutura FRAME (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7447e0ba8e13a593af6ac346ad47f8fe992b4a3187f0c46e8ee8fc28ddeb5646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910946"
---
# <a name="frame-structure"></a>Estrutura FRAME

A **estrutura FRAME** é um quadro real do driver.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Membros

<dl> <dt>

**Timestamp**
</dt> <dd>

Tempo decorrido, em microssegundos, entre o início da captura e a hora em que o quadro foi capturado.

</dd> <dt>

**FrameLength**
</dt> <dd>

Comprimento do quadro MAC.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Comprimento real do quadro copiado.

</dd> <dt>

**MacFrame**
</dt> <dd>

Dados de quadro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




