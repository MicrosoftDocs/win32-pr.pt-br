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
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756323"
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

*Elementos de* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que contém o tamanho de um elemento na lista.

</dd> <dt>

*ElementCount* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que contém o número de elementos na lista.

</dd> <dt>

*EventTrace* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de estruturas de **\_ rastreamento de \_ eventos \_ de descarga DPE** . Para obter mais informações, consulte Comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O carregador armazena informações de eventos descarregadas em locais que podem ser lidos entre processos aproveitando o fato de que Ntdll.dll é carregado no mesmo endereço base em todos os processos. Quando um depurador precisa consultar informações de módulo descarregadas, ele chama essa função para determinar o endereço no qual as variáveis residem e, em seguida, consulta a memória virtual no processo de destino nesses endereços para ler os valores reais.

Cada elemento na lista é definido da seguinte maneira.

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

Esta função não tem nenhum arquivo de cabeçalho associado. A biblioteca de importação associada, ntdll. lib, está disponível no Windows Driver Kit (WDK). Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
