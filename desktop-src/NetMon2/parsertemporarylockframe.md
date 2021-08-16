---
description: A função ParserTemporaryLockFrame bloqueia um quadro quando ele entra em um analisador e desbloqueia o quadro quando a função sai do analisador.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Função ParserTemporaryLockFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 47a8c02a29007084161897e34bd3ba6fbe3b5f53460aaced2acaf8e4924d67f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364382"
---
# <a name="parsertemporarylockframe-function"></a>Função ParserTemporaryLockFrame

A função **ParserTemporaryLockFrame** bloqueia um quadro quando ele entra em um analisador e desbloqueia o quadro quando a função sai do analisador.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro para o qual o analisador aponta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte de dados no quadro.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Os analisadores não devem chamar a função **LockFrame** . Se um analisador usar um bloqueio e, em seguida, gerar uma falha ou retornar sem desbloquear o quadro, o analisador deixará o sistema em um estado em que ele não possa alterar protocolos nem recortar ou copiar quadros. Os analisadores devem usar a função **ParserTemporaryLockFrame** , que concede um bloqueio somente durante o contexto da entrada da função no analisador. Ao sair do analisador, o bloqueio para esse quadro é liberado. Como resultado, o ponteiro será válido somente depois que o analisador retornar da chamada para a função **attachproperties** ou **RecognizeFrame** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




