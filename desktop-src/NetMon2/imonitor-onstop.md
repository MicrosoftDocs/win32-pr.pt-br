---
description: O método OnStop deve ser implementado pelo monitor. O MSCVC chama esse método para notificar o monitor de que a captura será interrompida.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: Método IMonitor::OnStop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: cb81042395de2a2381921cfd0b30c18af22df320b8ce8db228cf65743b1fe334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778986"
---
# <a name="imonitoronstop-method"></a>Método IMonitor::OnStop

O **método OnStop** deve ser implementado pelo monitor. O MSCVC chama esse método para notificar o monitor de que a captura será interrompida.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).

Se o método não for bem-sucedido, o valor de retorno será um código de erro. Quando um código de erro é retornado, o monitor não pode ser reiniciado.

## <a name="remarks"></a>Comentários

O MCSVC chama esse método depois [que IRTC::Stop](irtc-stop.md) é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




