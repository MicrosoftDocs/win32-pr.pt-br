---
description: A função ModifyFrame altera um quadro existente com novos dados.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Função ModifyFrame (Netmon. h)
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
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749239"
---
# <a name="modifyframe-function"></a>Função ModifyFrame

A função **ModifyFrame** altera um quadro existente com novos dados.

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

*hCapture* \[ no\]
</dt> <dd>

Identificador para a captura. Para obter informações sobre como obter o identificador de captura, consulte a seção comentários deste tópico do **ModifyFrame** .

</dd> <dt>

*FrameNumber* \[ no\]
</dt> <dd>

Número de índice do quadro.

</dd> <dt>

*FrameData* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de bytes que contém os novos dados de quadro.

</dd> <dt>

*FrameLength* \[ no\]
</dt> <dd>

Comprimento dos novos dados, em bytes.

</dd> <dt>

*Timestamp* \[ fora\]
</dt> <dd>

Carimbo de data/hora que indica quando o quadro foi modificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um identificador para um novo quadro.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Se a chamada for bem-sucedida, a função **ModifyFrame** destruirá o quadro original.

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **ModifyFrame** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




