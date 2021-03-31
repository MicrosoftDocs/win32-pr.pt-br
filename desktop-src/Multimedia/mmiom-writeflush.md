---
title: Mensagem de MMIOM_WRITEFLUSH (mmsystem. h)
description: A \_ mensagem MMIOM WRITEFLUSH é enviada a um procedimento de e/s pela função mmioWrite para solicitar que os dados sejam gravados em um arquivo aberto e que todos os buffers internos usados pelo procedimento de e/s sejam liberados para o disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- Multimídia do Windows de mensagem MMIOM_WRITEFLUSH
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645114"
---
# <a name="mmiom_writeflush-message"></a>\_Mensagem MMIOM WRITEFLUSH

A mensagem **MMIOM \_ WRITEFLUSH** é enviada a um procedimento de e/s pela função [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) para solicitar que os dados sejam gravados em um arquivo aberto e que todos os buffers internos usados pelo procedimento de e/s sejam liberados para o disco.


```C++
MMIOM_WRITEFLUSH 
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

Essa mensagem é equivalente à mensagem [**de \_ gravação MMIOM**](mmiom-write.md) , exceto pelo fato de que ela solicita que o procedimento de e/s libere seus buffers internos, se houver. A menos que um procedimento de e/s execute um buffer interno, essa mensagem pode ser tratada exatamente como a mensagem de **\_ gravação MMIOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

