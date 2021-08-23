---
title: MMIOM_SEEK mensagem (Mmsystem.h)
description: A mensagem MMIOM SEEK é enviada a um procedimento de E/S pela função mmioSeek para solicitar que a posição atual do arquivo \_ seja movida.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea33db15de3a4617561c437f2d5086afbf4bff2155e657677b171b1413b1c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065296"
---
# <a name="mmiom_seek-message"></a>Mensagem MMIOM \_ SEEK

A **mensagem MMIOM \_ SEEK** é enviada a um procedimento de E/S pela [**função mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) para solicitar que a posição atual do arquivo seja movida.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

Nova posição do arquivo. O significado desse valor depende do sinalizador especificado em **lChangeFlag.**

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

Sinalizador que especifica como a posição do arquivo é alterada. Os seguintes valores são definidos:



| Requisito | Valor |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| BUSCAR \_ CUR | Mova a posição do arquivo para *que seja lNewFilePos* bytes da posição atual. *lNewFilePos* pode ser positivo ou negativo. |
| FIM DA \_ BUSCA | Mova a posição do arquivo para *que seja lNewFilePos* bytes do final do arquivo.                                             |
| SEEK \_ SET | Mova a posição do arquivo para *que seja lNewFilePos* bytes do início do arquivo.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna a nova posição do arquivo. Se houver um erro, o valor de retorno será 1.

## <a name="remarks"></a>Comentários

O procedimento de E/S é responsável por manter a posição do arquivo atual no **membro lDiskOffset** da [**estrutura MMIOINFO.**](/previous-versions//dd757322(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

