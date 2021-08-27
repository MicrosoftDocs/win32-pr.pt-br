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
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058586"
---
# <a name="rtlgetunloadeventtrace-function"></a>Função RtlGetUnloadEventTrace

\[essa função pode ser alterada ou removida de Windows sem aviso prévio.\]

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

Esta função não tem nenhum arquivo de cabeçalho associado. a biblioteca de importação associada, Ntdll. lib, está disponível no Windows Driver Kit (WDK). Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
