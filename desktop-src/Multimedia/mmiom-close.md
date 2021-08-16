---
title: Mensagem de MMIOM_CLOSE (mmsystem. h)
description: A \_ mensagem de fechamento MMIOM é enviada a um procedimento de e/s pela função mmioClose para solicitar que um arquivo seja fechado.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- mensagem de MMIOM_CLOSE Windows multimídia
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a26b8b2ffa80c7c522fa5cdcbfc5da3334e0d2b5e258e090932147bf85438c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065386"
---
# <a name="mmiom_close-message"></a>MMIOM \_ fechar mensagem

A mensagem de **\_ fechamento MMIOM** é enviada a um procedimento de e/s pela função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para solicitar que um arquivo seja fechado.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

Sinalizadores contidos no parâmetro **wFlags** de **mmioClose**.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se o arquivo for fechado com êxito ou se um erro for diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

