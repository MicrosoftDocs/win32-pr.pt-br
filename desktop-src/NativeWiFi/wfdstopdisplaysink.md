---
description: Interrompe o Miracast do usuário, desliga a capacidade de descoberta e des registra o retorno de chamada.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Função WFDDisplaySinkStop (Wfdsink.h)
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
ms.openlocfilehash: a5e2da91e29535c1e2fd9553a2b6ec2bb0008e61f33cd55ebcda2746b93eb657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797925"
---
# <a name="wfddisplaysinkstop-function"></a>Função WFDDisplaySinkStop

Interrompe o Miracast do usuário, desliga a capacidade de descoberta e des registra o retorno de chamada. Seu aplicativo deve chamar isso uma vez no desligamento.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

## <a name="remarks"></a>Comentários

Espera-se que seu aplicativo desbloqueou todos os retornos de chamada em andamento antes de chamar **WFDStopDisplaySink.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows 10<br/>                                                                      |
| Fim do suporte ao servidor<br/>    | Windows Server 2016<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




