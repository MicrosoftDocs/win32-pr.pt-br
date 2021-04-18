---
description: A estrutura de acompanhamento de PF \_ define os protocolos que podem preceder ou seguir um protocolo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Estrutura de PF_FOLLOWSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757235"
---
# <a name="pf_followset-structure"></a>Estrutura de acompanhamento de PF \_

A estrutura de **\_ acompanhamento de PF** define os protocolos que podem preceder ou seguir um protocolo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>Membros

<dl> <dt>

**nEntries**
</dt> <dd>

Número de protocolos na lista.

</dd> <dt>

**Entrada**
</dt> <dd>

Matriz de [estruturas \_ FOLLOWENTRY de PF](pf-followentry.md) que descrevem cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de [ \_ PARSERINFO de PF](pf-parserinfo.md) usa a estrutura de **\_ acompanhamento de PF** para listar os protocolos que podem preceder ou seguir o protocolo que o analisador detecta.

Monitor de Rede usa as informações na estrutura do conjunto de **PP-PF \_** para atualizar os seguintes conjuntos de analisadores específicos. A estrutura de **\_ acompanhamento de PF** deve ser alocada usando **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FOLLOWENTRY de PF \_](pf-followentry.md)
</dt> <dt>

[PARSERINFO de PF \_](pf-parserinfo.md)
</dt> </dl>

 

 




