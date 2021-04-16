---
description: A estrutura HANDOFFENTRY define uma entrada de protocolo específica em uma estrutura de entrega.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Estrutura HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501347"
---
# <a name="handoffentry-structure"></a>Estrutura HANDOFFENTRY

A estrutura **HANDOFFENTRY** define uma entrada de protocolo específica em uma estrutura de **entrega** .

Essa estrutura é preenchida por Monitor de Rede com base nas informações de um arquivo. ini fornecido pelo usuário fornecido ao chamar a função [**Createentregatable**](createhandofftable.md) . Essa estrutura nunca deve ser modificada explicitamente por um aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_SIG como**
</dt> <dd>

Assinatura que identifica essa entrada como uma entrada de tabela de entrega.

</dd> <dt>

**como \_ ProtIdentNumber**
</dt> <dd>

Número de protocolo fornecido pelo arquivo. ini fornecido pelo usuário.

</dd> <dt>

**como \_ ProtocolHandle**
</dt> <dd>

Identificador de protocolo criado usando o nome do protocolo fornecido pelo arquivo. ini fornecido pelo usuário.

</dd> <dt>

**como \_ ProtocolData**
</dt> <dd>

Dados de instância de protocolo fornecidos pelo arquivo. ini fornecido pelo usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é preenchida por Monitor de Rede quando Monitor de Rede cria uma tabela de entrega.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ENTREGA](handofftable.md)
</dt> </dl>

 

 




