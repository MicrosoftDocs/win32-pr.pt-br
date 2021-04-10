---
description: A função GetFrameSrcAddressOffset retorna o deslocamento do endereço de origem dos quadros.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Função GetFrameSrcAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170661"
---
# <a name="getframesrcaddressoffset-function"></a>Função GetFrameSrcAddressOffset

A função **GetFrameSrcAddressOffset** retorna o deslocamento do endereço de origem do quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* 
</dt> <dd>

Identificador para o quadro.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo de endereço de origem. O valor do parâmetro pode ser um dos seguintes:

-   tipo de endereço \_ \_ Ethernet
-   \_IP do tipo de endereço \_
-   tipo de endereço \_ \_ IPX
-   tipo de endereço \_ \_ TOKENRING
-   tipo de endereço \_ \_ FDDI
-   tipo de endereço \_ \_ XNS
-   \_IP de \_ Vines de tipo de endereço \_
-   tipo de endereço \_ \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Ponteiro para uma **DWORD**, que, em retorno, contém o comprimento do endereço, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será o deslocamento para o endereço de origem.

Se a função não for bem-sucedida, o valor de retorno será menos um (-1).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




