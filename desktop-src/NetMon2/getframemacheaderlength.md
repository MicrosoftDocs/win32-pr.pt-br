---
description: A função GetFrameMacHeaderLength retorna o comprimento, em bytes, do cabeçalho MAC do quadro.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Função GetFrameMacHeaderLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0e6c4abe859cd4c307d8ade586b9371b69b5c171681006cf4aa1634ef815d794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743896"
---
# <a name="getframemacheaderlength-function"></a>Função GetFrameMacHeaderLength

A função **GetFrameMacHeaderLength** retorna o comprimento, em bytes, do cabeçalho Mac do quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será o comprimento em bytes do cabeçalho MAC.

Se a função não for bem-sucedida ou se um tipo de MAC desconhecido for encontrado, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameMacHeaderLength** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




