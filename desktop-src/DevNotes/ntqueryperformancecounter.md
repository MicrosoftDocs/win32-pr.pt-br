---
description: Retorna o valor atual de um contador de desempenho e, opcionalmente, a frequência do contador de desempenho.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Função NtQueryPerformanceCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9c92863adbc0865700dad272bbc299e1f1a667b2fd4afbcd75d548e3330890b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667223"
---
# <a name="ntqueryperformancecounter-function"></a>Função NtQueryPerformanceCounter

\[Não há suporte para essa função e não deve ser usada. Use as **funções QueryPerformanceCounter** e **QueryPerformanceFrequency.**\]

Retorna o valor atual de um contador de desempenho e, opcionalmente, a frequência do contador de desempenho.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PerformanceCounter* \[ out\]
</dt> <dd>

O endereço de uma variável para receber o valor atual do contador de desempenho.

</dd> <dt>

*PerformanceFrequency* \[ out, opcional\]
</dt> <dd>

O endereço de uma variável para receber a frequência do contador de desempenho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará o código **NTSTATUS** **STATUS \_ SUCCESS**; caso contrário, retornará um código de erro como **STATUS ACCESS \_ \_ VIOLATION**.

## <a name="remarks"></a>Comentários

Nenhum arquivo de header está disponível para **NtQueryPerformanceCounter.** Você deve usar as funções alternativas nomeadas acima, embora você também possa usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

A frequência de desempenho é a frequência do contador de desempenho em hertz, especificamente em contagens por segundo. Esse valor depende da implementação. Se a implementação não tiver hardware para dar suporte ao tempo de desempenho, o valor retornado será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Queryperformancecounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
