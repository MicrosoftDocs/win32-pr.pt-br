---
description: A função ModifyFrame altera um quadro existente com novos dados.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Função ModifyFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 04bc22af11d83078ecf98d0386b061b520fbf9a8dcab6f6beb360c45b1c6fe96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555816"
---
# <a name="modifyframe-function"></a>Função ModifyFrame

A **função ModifyFrame** altera um quadro existente com novos dados.

## <a name="syntax"></a>Sintaxe


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCapture* \[ Em\]
</dt> <dd>

Lidar com a captura. Para obter informações sobre como obter o alça de captura, consulte a seção Comentários deste tópico **ModifyFrame.**

</dd> <dt>

*FrameNumber* \[ Em\]
</dt> <dd>

Número do índice do quadro.

</dd> <dt>

*FrameData* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de bytes que contêm os novos dados de quadro.

</dd> <dt>

*FrameLength* \[ Em\]
</dt> <dd>

Comprimento dos novos dados, em bytes.

</dd> <dt>

*TimeStamp* \[ out\]
</dt> <dd>

Carimbo de data/hora que indica quando o quadro foi modificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um handle para um novo quadro.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

Se a chamada for bem-sucedida, **a função ModifyFrame** destruirá o quadro original.

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função ModifyFrame.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




