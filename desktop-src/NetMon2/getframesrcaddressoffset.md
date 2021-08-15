---
description: A função GetFrameSrcAddressOffset retorna o deslocamento do endereço de origem dos quadros.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Função GetFrameSrcAddressOffset (Netmon.h)
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
ms.openlocfilehash: 5c8c2315b53d336a06a73e63019daee842439f65aa53e3fb7d34d4944dcab9cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366090"
---
# <a name="getframesrcaddressoffset-function"></a>Função GetFrameSrcAddressOffset

A **função GetFrameSrcAddressOffset** retorna o deslocamento do endereço de origem do quadro.

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

Lidar com o quadro.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo de endereço de origem. O valor do parâmetro pode ser um dos seguintes:

-   ETHERNET \_ DE TIPO DE \_ ENDEREÇO
-   \_IP DO TIPO DE \_ ENDEREÇO
-   \_TIPO DE ENDEREÇO \_ IPX
-   TOKENRING \_ DE TIPO \_ DE ENDEREÇO
-   TIPO \_ DE \_ ENDEREÇO FDDI
-   TIPO \_ DE \_ ENDEREÇO XNS
-   IP \_ \_ VINES DE TIPO DE \_ ENDEREÇO
-   ATM \_ DE \_ TIPO DE ENDEREÇO

</dd> <dt>

*AddressLength* 
</dt> <dd>

Ponteiro para um **DWORD**, que, no retorno, contém o comprimento do endereço, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será o deslocamento para o endereço de origem.

Se a função não for bem-sucedida, o valor de retorno será menos um (-1).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




