---
description: Multiplica os inteiros estendidos.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Função RtlExtendedIntegerMultiply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755511"
---
# <a name="rtlextendedintegermultiply-function"></a>Função RtlExtendedIntegerMultiply

\[A função **RtlExtendedIntegerMultiply** é exportada para dar suporte a binários de driver existentes e é obsoleta. Para obter um melhor desempenho, use o suporte do compilador para operações de inteiro de 64 bits.\]

Multiplica os inteiros estendidos.

## <a name="syntax"></a>Sintaxe


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Multiplicando* \[ no\]
</dt> <dd>

Multiplicando.

</dd> <dt>

*Multiplicador* \[ no\]
</dt> <dd>

Multiplicador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o resultado da multiplicação.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
