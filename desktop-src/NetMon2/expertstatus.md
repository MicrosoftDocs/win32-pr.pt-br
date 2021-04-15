---
description: Indica o status atual de um especialista em execução.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Estrutura EXPERTSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501357"
---
# <a name="expertstatus-structure"></a>Estrutura EXPERTSTATUS

A estrutura **EXPERTSTATUS** indica o status atual de um especialista em execução.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Status**
</dt> <dd>

Valor de status de especialista atual definido pela enumeração [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .

</dd> <dt>

**SubStatus**
</dt> <dd>

Valor de substatus.

</dd> <dt>

**PercentDone**
</dt> <dd>

Porcentagem de conclusão da análise do especialista de dados de rede.

</dd> <dt>

**Frame**
</dt> <dd>

Número do quadro.

</dd> <dt>

**szStatusText**
</dt> <dd>

Texto que descreve o status do especialista.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




