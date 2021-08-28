---
title: MPSTATUS_DATA estrutura (MpClient.h)
description: Contém dados sobre o status atual de um componente do produto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA estrutura herdada Windows recursos de ambiente
- PMPSTATUS_DATA de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78989b055e6de79c3da733ff8bc498a3fb6717c5dec226db73b80c4e5c9d899c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887906"
---
# <a name="mpstatus_data-structure"></a>Estrutura DE DADOS \_ MPSTATUS

Contém dados sobre o status atual de um componente do produto.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**ComponentID**
</dt> <dd>

Tipo: **[ **\_ ID MPCOMPONENT**](mpcomponent-id.md)**

</dd> <dd>

ID de componente específica para a qual o status é relatado.

</dd> <dt>

**fEnable**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

Status solicitado para o componente. **hResult nos** dados de retorno de chamada significa êxito ou falha para a solicitação.

</dd> <dt>

**ComponentStatus**
</dt> <dd>

Dados de status extras, dependendo do valor **de ComponentID.**

> [!Note]  
> Atualmente, resulta em um ponteiro para uma estrutura fiada para todos os valores possíveis de **ComponentID.**

 

<dl> <dt>

**p1**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ AS \_ SIGNATURE**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p2**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ AV \_ SIGNATURE**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p3**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ REALTIME \_ MONITOR**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p4**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ ONACCESS \_ PROTECTION**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p5**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ PROTECTION**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p6**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ BEHAVIOR \_ MONITOR**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p7**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ AUTO \_ SCAN**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p8**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ AUTO \_ SIGUPDATE**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p9**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ IPC**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**Pa**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **COMPONENTID**  ==  **MPCOMPONENT \_ NIS**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**pb**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ ELAM**. Consulte [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID DO MPCOMPONENT \_**](mpcomponent-id.md)
</dt> <dt>

[**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





