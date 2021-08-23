---
description: Recupera o tamanho e o local da lista de módulos descarregados dinamicamente para o processo atual.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Função RtlGetUnloadEventTraceEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 35c4001851cc12701152f983c51a800d8f1846e015f5cf4d967c6371d9807578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571356"
---
# <a name="rtlgetunloadeventtraceex-function"></a>Função RtlGetUnloadEventTraceEx

Recupera o tamanho e o local da lista de módulos descarregados dinamicamente para o processo atual.

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ElementSize* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que contém o tamanho de um elemento na lista.

</dd> <dt>

*ElementCount* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que contém o número de elementos na lista.

</dd> <dt>

*EventTrace* \[ out\]
</dt> <dd>

Um ponteiro para uma matriz de estruturas **\_ RTL UNLOAD \_ EVENT \_ TRACE.** Para obter mais informações, consulte Comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O carregador armazena informações de evento descarregadas em locais que podem ser lidos entre processos, aproveitando o fato de que Ntdll.dll é carregado no mesmo endereço base em todos os processos. Quando um depurador precisa consultar informações de módulo descarregado, ele chama essa função para determinar o endereço no qual residem as variáveis e, em seguida, consulta a memória virtual no processo de destino nesses endereços para ler os valores reais.

Cada elemento na lista é definido da seguinte forma.

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

Essa função não tem nenhum arquivo de header associado. A biblioteca de importação associada, Ntdll.lib, está disponível no WDK (Kit Windows Driver). Você também pode chamar essa função usando as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
