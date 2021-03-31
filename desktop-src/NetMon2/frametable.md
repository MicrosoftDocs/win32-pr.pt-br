---
description: A estrutura de FRAMEtable, um buffer circular de ponteiros de quadro, é devolvido aos aplicativos anexados à interface ITRC do NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Estrutura de FRAMEtable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089972"
---
# <a name="frametable-structure"></a>Estrutura de quadros

A estrutura de **frametable** , um buffer circular de ponteiros de quadro, é devolvido aos aplicativos anexados à interface **ITRC** do NPP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**FrameTableLength**
</dt> <dd>

O comprimento total da tabela.

</dd> <dt>

**StartIndex**
</dt> <dd>

O primeiro índice na tabela.

</dd> <dt>

**EndIndex**
</dt> <dd>

O último índice na tabela.

</dd> <dt>

**FrameCount**
</dt> <dd>

O número de quadros descritos por esta tabela.

</dd> <dt>

**Intervalos**
</dt> <dd>

A matriz real de descritores de quadros.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




