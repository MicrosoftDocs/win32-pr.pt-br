---
description: A função GetFrame retorna um identificador para um determinado quadro dentro de uma captura.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Função GetFrame (Netmon. h)
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
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089967"
---
# <a name="getframe-function"></a>Função GetFrame

A função **GetFrame** retorna um identificador para um determinado quadro dentro de uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCapture* \[ no\]
</dt> <dd>

Identificador para uma captura. Para obter o identificador de captura, chame a função [GetFrameCaptureHandle](getframecapturehandle.md) .

</dd> <dt>

*FrameNumber* \[ no\]
</dt> <dd>

Número (baseado em zero) do quadro. O número do primeiro quadro em uma captura é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um identificador para o quadro.

Se a função não for bem-sucedida (ou seja, se *hCapture* for inválido ou o número do quadro estiver fora do intervalo), o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Use a função **GetFrame** para obter o identificador de quadro necessário ao localizar instâncias de uma propriedade. As funções usadas para localizar as instâncias de propriedade são [FindPropertyInstance](findpropertyinstance.md) que localiza a primeira instância e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) que localiza a próxima instância.

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrame** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




