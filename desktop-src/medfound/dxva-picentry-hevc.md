---
description: Especifica uma referência a uma superfície não compactada.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Estrutura de DXVA_PicEntry_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749517"
---
# <a name="dxva_picentry_hevc-structure"></a>Estrutura de HEVC de DXVA \_ PicEntry \_

Especifica uma referência a uma superfície não compactada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Index7Bits**
</dt> <dd>

Um índice que identifica uma superfície não compactada.

</dd> <dt>

**AssociatedFlag** 
</dt> <dd>

Sinalizador de 1 bit opcional associado à superfície. O significado do sinalizador depende do contexto. Por exemplo, ele pode especificar se o quadro de referência é uma referência de longo prazo ou uma referência de curto prazo.

</dd> <dt>

**bPicEntry**
</dt> <dd>

Acessa todos os 8 bits da União.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




