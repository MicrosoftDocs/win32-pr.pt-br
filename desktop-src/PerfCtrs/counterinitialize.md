---
description: Registra o provedor e inicializa os conjuntos de contadores.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Função de reinicialização
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: e7c2fb61b53ca1847eefcc453a91f69b3c0602e06277b4858b8f0b733be7f71b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517676"
---
# <a name="counterinitialize-function"></a>Função de reinicialização

Registra o provedor e inicializa os conjuntos de contadores.

## <a name="syntax"></a>Sintaxe


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna \_ o êxito do erro em caso de sucesso; caso contrário, um código de erro Win32 padrão.

## <a name="remarks"></a>Comentários

Seu provedor chama essa função. A função inclui chamadas para a função [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) e a função [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .

A ferramenta [**ctrpp**](ctrpp.md) gera essa função embutida quando você especifica o argumento **-o** . O nome da função inclui uma cadeia de caracteres de *prefixo* se você especificar o argumento **-prefix** .

Se você especificar os argumentos **-MemoryRoutines** ou **-NotificationCallback** (ou especificar o atributo de **retorno de chamada** para o elemento [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), a assinatura de **metainicialização** será alterada para o seguinte:

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

onde:

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback
</dt> <dd>

O nome da função de retorno de chamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que você implementa para receber a notificação de solicitações de consumidor (por exemplo, solicitações para adicionar ou remover contadores da consulta). Defina como **NULL** se você não implementar a função de retorno de chamada *ControlCallback* .

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

O nome da função de retorno de chamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) que o PERFLIB chama para alocar memória. Defina como **NULL** se você não tiver especificado o argumento **-MemoryRoutines** .

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

O nome da função de retorno de chamada [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) que o PERFLIB chama para liberar a memória alocada usando a função [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) . Defina como **NULL** se *MemoryAllocationFunction* for **nulo**.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext
</dt> <dd>

Informações de contexto a serem passadas para sua alocação de memória e rotinas gratuitas. Pode ser **NULL**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



 

