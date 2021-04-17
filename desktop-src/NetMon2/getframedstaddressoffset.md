---
description: A função GetFrameDstAddressOffset retorna o deslocamento para o endereço de destino de um determinado quadro.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Função GetFrameDstAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775675"
---
# <a name="getframedstaddressoffset-function"></a>Função GetFrameDstAddressOffset

A função **GetFrameDstAddressOffset** retorna o deslocamento para o endereço de destino de um determinado quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro.

</dd> <dt>

*AddressType* \[ no\]
</dt> <dd>

Tipo do endereço de destino. Especifique um dos seguintes valores:

tipo de endereço endereço Ethernet tipo de endereço IP tipo de endereço \_ \_ \_ \_ \_ \_ IPX \_ tipo de \_ endereço TOKENRING \_ tipo \_ \_ \_ \_ \_ \_ \_ \_ do endereço FDDI tipo de endereço do XNS tipo de endereços IP tipo de endereço ATM.

</dd> <dt>

*AddressLength* \[ no\]
</dt> <dd>

Comprimento do endereço de destino, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será o deslocamento (medido em bytes) para o tipo de endereço solicitado.

Se a função não for bem-sucedida, o valor de retorno será menos um (-1).

## <a name="remarks"></a>Comentários

Se o parâmetro *AddressType* for definido como tipo de endereço \_ \_ Ethernet, o valor de retorno da função **GetFrameDstAddressOffset** será sempre zero. O deslocamento de um endereço Ethernet é sempre zero.

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameDstAddressOffset** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




