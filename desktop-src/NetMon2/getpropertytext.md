---
description: A função GetPropertyText retorna um ponteiro para o texto da propriedade.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Função GetPropertyText (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b92bf854dd4a3e678a4eb5524bd47412f012da87a007e960498d11d4bff91ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982050"
---
# <a name="getpropertytext-function"></a>Função GetPropertyText

A função **GetPropertyText** retorna um ponteiro para o texto da propriedade.

## <a name="syntax"></a>Sintaxe


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro.

</dd> <dt>

*lpPI* \[ no\]
</dt> <dd>

Ponteiro para uma instância de propriedade.

</dd> <dt>

*szBuffer* \[ no\]
</dt> <dd>

Ponteiro para a cadeia de texto da propriedade.

</dd> <dt>

*BufferSize* \[ no\]
</dt> <dd>

Tamanho do buffer de cadeia de texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o texto da propriedade.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetPropertyText** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




