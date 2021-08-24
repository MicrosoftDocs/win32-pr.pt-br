---
description: A função GetFrame retorna um handle para um determinado quadro dentro de uma captura.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Função GetFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5f6f992c0c61978e2de6f90755852c9e29d6ac51d7ae7f2405ef981ed695c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779246"
---
# <a name="getframe-function"></a>Função GetFrame

A **função GetFrame** retorna um handle para um determinado quadro dentro de uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCapture* \[ Em\]
</dt> <dd>

Lidar com uma captura. Para obter o alça de captura, chame a [função GetFrameCaptureHandle.](getframecapturehandle.md)

</dd> <dt>

*FrameNumber* \[ Em\]
</dt> <dd>

Número (baseado em zero) do quadro. O número do primeiro quadro em uma captura é zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um handle para o quadro.

Se a função não for bem-sucedida (ou seja, se *hCapture* for inválido ou o número do quadro estiver fora do intervalo), o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

Use a **função GetFrame** para obter o alça de quadro necessário ao localizar instâncias de uma propriedade. As funções usadas para localizar instâncias de propriedade [são FindPropertyInstance,](findpropertyinstance.md) que localiza a primeira instância, e [FindPropertyInstanceRestart,](findpropertyinstancerestart.md) que localiza a próxima instância.

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função GetFrame.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




