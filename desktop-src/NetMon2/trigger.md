---
description: A estrutura do gatilho indica uma ação a ser tomada pelo driver em um horário especificado.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Estrutura do gatilho (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758450"
---
# <a name="trigger-structure"></a>Estrutura do gatilho

A estrutura do **gatilho** indica uma ação a ser tomada pelo driver em um horário especificado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>Membros

<dl> <dt>

**TriggerActive**
</dt> <dd>

Um valor booliano que determina se o gatilho deve ser pago pelo driver.

</dd> <dt>

**TriggerType**
</dt> <dd>

O código op do gatilho.

</dd> <dt>

**TriggerAction**
</dt> <dd>

Ação que o gatilho deve tomar se for acionado.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Sinalizadores de gatilho.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

A correspondência do padrão de gatilho.

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

Tamanho do buffer de gatilho.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




