---
title: Mensagem de MMIOM_CLOSE (mmsystem. h)
description: A \_ mensagem de fechamento MMIOM é enviada a um procedimento de e/s pela função mmioClose para solicitar que um arquivo seja fechado.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- Multimídia do Windows de mensagem MMIOM_CLOSE
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
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499860"
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



 

