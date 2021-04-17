---
description: Um quadro real do driver.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Estrutura do quadro (Netmon. h)
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
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766364"
---
# <a name="frame-structure"></a>Estrutura do quadro

A estrutura do **quadro** é um quadro real do driver.

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

**Estampa**
</dt> <dd>

Tempo decorrido, em microssegundos, entre o início da captura e a hora em que o quadro foi capturado.

</dd> <dt>

**FrameLength**
</dt> <dd>

Tamanho do quadro MAC.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Tamanho de quadro real copiado.

</dd> <dt>

**MacFrame**
</dt> <dd>

Dados do quadro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




