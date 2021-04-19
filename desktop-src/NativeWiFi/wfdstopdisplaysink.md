---
description: Interrompe o modo de coletor Miracast, desativa a descoberta e cancela o registro do retorno de chamada.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Função WFDDisplaySinkStop (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770152"
---
# <a name="wfddisplaysinkstop-function"></a>Função WFDDisplaySinkStop

Interrompe o modo de coletor Miracast, desativa a descoberta e cancela o registro do retorno de chamada. Seu aplicativo deve chamá-lo uma vez durante o desligamento.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

## <a name="remarks"></a>Comentários

Espera-se que seu aplicativo tenha desbloqueado quaisquer retornos de chamada em andamento antes de chamar **WFDStopDisplaySink**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 10<br/>                                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2016<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




