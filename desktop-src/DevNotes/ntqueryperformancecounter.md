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
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754461"
---
# <a name="ntqueryperformancecounter-function"></a>Função NtQueryPerformanceCounter

\[Essa função não tem suporte e não deve ser usada. Em vez disso, use as funções **QueryPerformanceCounter** e **QueryPerformanceFrequency** .\]

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

*PerformanceCounter* \[ fora\]
</dt> <dd>

O endereço de uma variável para receber o valor do contador de desempenho atual.

</dd> <dt>

*PerformanceFrequency* \[ out, opcional\]
</dt> <dd>

O endereço de uma variável para receber a frequência do contador de desempenho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará o status de código de **NTSTATUS** **\_ Success**; caso contrário, retornará um código de erro como **status \_ \_ violação de acesso**.

## <a name="remarks"></a>Comentários

Nenhum arquivo de cabeçalho está disponível para **NtQueryPerformanceCounter**. Você deve usar as funções alternativas nomeadas acima, embora também possa usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

Frequência de desempenho é a frequência do contador de desempenho em Hertz, especificamente em contagens por segundo. Esse valor é dependente de implementação. Se a implementação não tiver hardware para dar suporte ao tempo de desempenho, o valor retornado será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
