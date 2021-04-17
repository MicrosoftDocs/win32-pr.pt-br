---
description: A função LoadStringAddr transforma uma cadeia de caracteres (como &\# 0034; 157.54.32.45&\# 0034;) e cria um endereço DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Função LoadStringAddr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770142"
---
# <a name="loadstringaddr-function"></a>Função LoadStringAddr

A função **LoadStringAddr** transforma uma cadeia de caracteres (como "157.54.32.45") e cria um endereço **DWORD** .

## <a name="syntax"></a>Sintaxe


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAddress* 
</dt> <dd>

Ponteiro para um **DWORD**.

</dd> <dt>

*str* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres com a representação x. x. x de um endereço IP (por exemplo, 127.0.0.1).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (o nome do endereço foi encontrado); o valor de retorno é **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




