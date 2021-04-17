---
title: Mensagem de MMIOM_SEEK (mmsystem. h)
description: A mensagem de busca do MMIOM \_ é enviada a um procedimento de e/s pela função mmioSeek para solicitar que a posição atual do arquivo seja movida.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- Multimídia do Windows de mensagem MMIOM_SEEK
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
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761891"
---
# <a name="mmiom_seek-message"></a>Mensagem de busca do MMIOM \_

A mensagem de **\_ busca do MMIOM** é enviada a um procedimento de e/s pela função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) para solicitar que a posição atual do arquivo seja movida.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

Nova posição do arquivo. O significado desse valor é dependente do sinalizador especificado em **lChangeFlag**.

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

Sinalizador que especifica como a posição do arquivo é alterada. Os seguintes valores são definidos:



| Requisito | Valor |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| BUSCAR em \_ cur | Mova a posição do arquivo para ser *lNewFilePos* bytes da posição atual. *lNewFilePos* pode ser positivo ou negativo. |
| fim da busca \_ | Mova a posição do arquivo para ser *lNewFilePos* bytes do final do arquivo.                                             |
| conjunto de busca \_ | Mova a posição do arquivo para ser *lNewFilePos* bytes do início do arquivo.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna a nova posição do arquivo. Se houver um erro, o valor de retorno será 1.

## <a name="remarks"></a>Comentários

O procedimento de e/s é responsável por manter a posição atual do arquivo no membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

