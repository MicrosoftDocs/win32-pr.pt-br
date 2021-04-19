---
description: Divide inteiros estendidos.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: Função RtlExtendedLargeIntegerDivide
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756509"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>Função RtlExtendedLargeIntegerDivide

\[A função **RtlExtendedLargeIntegerDivide** é exportada para dar suporte a binários de driver existentes e é obsoleta. Para obter um melhor desempenho, use o suporte do compilador para operações de inteiro de 64 bits.\]

Divide inteiros estendidos.

## <a name="syntax"></a>Sintaxe


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dividendo* \[ no\]
</dt> <dd>

Cheque.

</dd> <dt>

*Divisor* \[ no\]
</dt> <dd>

Divisor.

</dd> <dt>

*Restante* \[ entrada, saída\]
</dt> <dd>

Ponteiro para a divisão restante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o resultado da operação de divisão.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
