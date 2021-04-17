---
description: Permite que o código de despejo obtenha as informações do módulo descarregado de Ntdll.dll para armazenamento no minidespejo.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Função RtlGetUnloadEventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748686"
---
# <a name="rtlgetunloadeventtrace-function"></a>Função RtlGetUnloadEventTrace

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Permite que o código de despejo obtenha as informações do módulo descarregado de Ntdll.dll para armazenamento no minidespejo.

## <a name="syntax"></a>Sintaxe


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função retorna um ponteiro para uma matriz. Para obter mais informações, consulte Comentários.

## <a name="remarks"></a>Comentários

A matriz RtlpUnloadEventTrace é definida da seguinte maneira:

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

Esta função não tem nenhum arquivo de cabeçalho associado. A biblioteca de importação associada, ntdll. lib, está disponível no Windows Driver Kit (WDK). Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
