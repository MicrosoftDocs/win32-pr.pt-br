---
title: MMIOM_WRITEFLUSH mensagem (Mmsystem.h)
description: A mensagem MMIOM WRITEFLUSH é enviada a um procedimento de E/S pela função mmioWrite para solicitar que os dados sejam gravados em um arquivo aberto e que quaisquer buffers internos usados pelo procedimento de E/S sejam liberados para o \_ disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH mensagem Windows Multimídia
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
ms.openlocfilehash: b274536e934f426ef5e545e758c2f7bf918d552c42085650fc7c81a6a47c842e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807086"
---
# <a name="mmiom_writeflush-message"></a>Mensagem MMIOM \_ WRITEFLUSH

A mensagem **MMIOM \_ WRITEFLUSH** é enviada a um procedimento de E/S pela função [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) para solicitar que os dados sejam gravados em um arquivo aberto e que quaisquer buffers internos usados pelo procedimento de E/S sejam liberados para o disco.


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*Lpbuffer*
</dt> <dd>

Ponteiro para um buffer que contém os dados a gravar no arquivo.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Número de bytes a gravar no arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o número de bytes realmente gravados no arquivo. Se houver um erro, o valor de retorno será 1.

## <a name="remarks"></a>Comentários

O procedimento de E/S é responsável por atualizar o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para refletir a nova posição do arquivo após a operação de gravação.

Essa mensagem é equivalente à mensagem [**WRITE MMIOM, \_**](mmiom-write.md) exceto que solicita que o procedimento de E/S libera seus buffers internos, se algum. A menos que um procedimento de E/S execute o buffer interno, essa mensagem pode ser tratada exatamente como a **mensagem MMIOM \_ WRITE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

