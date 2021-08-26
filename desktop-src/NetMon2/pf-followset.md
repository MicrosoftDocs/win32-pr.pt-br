---
description: A estrutura PF \_ FOLLOWSET define os protocolos que podem preceder ou seguir um protocolo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: PF_FOLLOWSET (Netmon.h)
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
ms.openlocfilehash: d404e602e78452a38343a6e62fce8c5b16941270eaa2825de8339f583c064a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036826"
---
# <a name="pf_followset-structure"></a>Estrutura \_ FOLLOWSET do PF

A **estrutura PF \_ FOLLOWSET** define os protocolos que podem preceder ou seguir um protocolo.

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

Matriz de [estruturas \_ FOLLOWENTRY do PF](pf-followentry.md) que descrevem cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [estrutura \_ PARSERINFO](pf-parserinfo.md) do PF usa a estrutura **PF \_ FOLLOWSET** para listar os protocolos que podem preceder ou seguir o protocolo detectado pelo analisador.

Monitor de Rede usa as informações na estrutura **\_ FOLLOWSET do PF** para atualizar os conjuntos de analisadores específicos a seguir. A **estrutura PF \_ FOLLOWSET** deve ser alocada usando **HeapAlloc.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




