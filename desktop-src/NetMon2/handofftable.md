---
description: A estrutura de ENTREGAtable define os protocolos de uma tabela de entrega.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Estrutura de ENTREGAtable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756885"
---
# <a name="handofftable-structure"></a>Estrutura de entrega

A estrutura de **entregatable** define os protocolos de uma tabela de entrega.

Essa estrutura é preenchida por Monitor de Rede com base nas informações de um arquivo. ini fornecido pelo usuário fornecido ao chamar a função [**Createentregatable**](createhandofftable.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_assinatura quente**
</dt> <dd>

Assinatura que identifica essa tabela como uma tabela de entrega.

</dd> <dt>

**\_NumEntries quente**
</dt> <dd>

Número de entradas que Monitor de Rede adicionadas à tabela entrega.

</dd> <dt>

**entradas de acesso \_**
</dt> <dd>

Tabela de entrega.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura, e suas estruturas HANDOFFENTRY associadas, são preenchidas por Monitor de Rede quando Monitor de Rede cria uma tabela de entrega.

As informações de protocolo usadas ao criar uma tabela de entrega são fornecidas em um arquivo. ini fornecido pelo aplicativo quando [**Createentregatable**](createhandofftable.md) é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[HANDOFFENTRY](handoffentry.md)
</dt> <dt>

[Createentregatable](createhandofftable.md)
</dt> </dl>

 

 




