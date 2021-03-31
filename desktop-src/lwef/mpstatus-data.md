---
title: Estrutura de MPSTATUS_DATA (MpClient. h)
description: Contém dados sobre o status atual de um componente do produto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSTATUS_DATA
- Ponteiro de estrutura de PMPSTATUS_DATA recursos de ambiente herdados do Windows
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
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644850"
---
# <a name="mpstatus_data-structure"></a>\_Estrutura de dados MPSTATUS

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

Tipo: **[ **\_ ID de MPCOMPONENT**](mpcomponent-id.md)**

</dd> <dd>

ID do componente específico para o qual o status é relatado.

</dd> <dt>

**fEnable**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

Status solicitado para o componente. **HRESULT** nos dados de retorno de chamada significa êxito ou falha para a solicitação.

</dd> <dt>

**ComponentStatus**
</dt> <dd>

Dados de status adicionais, dependendo do valor de **ComponentID**.

> [!Note]  
> Atualmente resulta em um ponteiro para uma estrutura fictícia para todos os valores possíveis de **ComponentID**.

 

<dl> <dt>

**P1**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ como \_ assinatura**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P2**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ a \_ assinatura do AV**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P3**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ o \_ Monitor em tempo real**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P4**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT a \_ \_ proteção do OnAccess**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P5**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ Protection**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P6**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ comportamento \_ Monitor**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P7**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ \_ verificação automática**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P8**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ \_ SIGUPDATE automático**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**P9**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ IPC**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**pa**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ NIS**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> <dt>

**PB**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ Elam**. Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ID do MPCOMPONENT \_**](mpcomponent-id.md)
</dt> <dt>

[**MPSTATUS \_ DATAEX \_ não usado**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





