---
description: A estrutura de FOLLOWENTRY do PF \_ define um protocolo que monitor de rede adiciona ao conjunto de acompanhamento de um analisador.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Estrutura de PF_FOLLOWENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828961"
---
# <a name="pf_followentry-structure"></a>Estrutura de FOLLOWENTRY de PF \_

A estrutura de **\_ FOLLOWENTRY do PF** define um protocolo que monitor de rede adiciona ao conjunto de acompanhamento de um analisador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**szProtocol**
</dt> <dd>

O nome do protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de [ \_ acompanhamento de PF](pf-followset.md) usa uma matriz de estruturas **\_ FOLLOWENTRY de PF** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[seguir do PF \_](pf-followset.md)
</dt> </dl>

 

 




