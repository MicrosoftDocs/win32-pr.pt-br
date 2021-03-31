---
description: A função BERGetInteger decodifica um inteiro codificado no BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Função BERGetInteger (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829343"
---
# <a name="bergetinteger-function"></a>Função BERGetInteger

A função **BERGetInteger** decodifica um inteiro codificado no ber.

## <a name="syntax"></a>Sintaxe


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Ponteiro para o número inteiro que é decodificado.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Ponteiro para o ponteiro para o valor retornado.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Ponteiro para o comprimento do cabeçalho retornado.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Ponteiro para o comprimento dos dados.

</dd> <dt>

*ppNext* 
</dt> <dd>

Ponteiro para o ponteiro para a próxima entrada do BER.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, se um inteiro codificado válido do BER for encontrado e convertido), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




