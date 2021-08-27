---
description: A estrutura PROTOCOLTABLE contém uma lista de protocolos.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Estrutura PROTOCOLTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a30d890fa5b6dcbbca1797a53722b97b2109cc9943ce07260c7f47514cfeb7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036976"
---
# <a name="protocoltable-structure"></a>Estrutura PROTOCOLTABLE

A **estrutura PROTOCOLTABLE** contém uma lista de protocolos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**nProtocols**
</dt> <dd>

Número de protocolos habilitados.

</dd> <dt>

**hProtocol**
</dt> <dd>

Matriz de alças para protocolos habilitados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




