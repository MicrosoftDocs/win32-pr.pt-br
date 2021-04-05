---
title: Mensagem de MMIOM_WRITE (mmsystem. h)
description: A \_ mensagem de gravação MMIOM é enviada a um procedimento de e/s pela função mmioWrite para solicitar que os dados sejam gravados em um arquivo aberto.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- Multimídia do Windows de mensagem MMIOM_WRITE
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919066"
---
# <a name="mmiom_write-message"></a>MMIOM \_ gravar mensagem

A mensagem de **\_ gravação MMIOM** é enviada a um procedimento de e/s pela função [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) para solicitar que os dados sejam gravados em um arquivo aberto.


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Ponteiro para um buffer que contém os dados a serem gravados no arquivo.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Número de bytes a serem gravados no arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o número de bytes realmente gravados no arquivo. Se houver um erro, o valor de retorno será 1.

## <a name="remarks"></a>Comentários

O procedimento de e/s é responsável por atualizar o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para refletir a nova posição do arquivo após a operação de gravação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

