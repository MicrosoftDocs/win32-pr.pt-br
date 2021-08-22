---
title: Mensagem de MMIOM_READ (mmsystem. h)
description: A \_ mensagem de leitura MMIOM é enviada a um procedimento de e/s pela função mmioRead para solicitar que um número especificado de bytes seja lido a partir de um arquivo aberto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- mensagem de MMIOM_READ Windows multimídia
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf5bbdbb20e2bc168f93857a7d59016197ccc4142d4ba18a2e6fd80842ff06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065346"
---
# <a name="mmiom_read-message"></a>MMIOM \_ ler mensagem

A mensagem de **\_ leitura MMIOM** é enviada a um procedimento de e/s pela função [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) para solicitar que um número especificado de bytes seja lido a partir de um arquivo aberto.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*
</dt> <dd>

Ponteiro para o buffer a ser preenchido com dados lidos do arquivo.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*
</dt> <dd>

Número de bytes a serem lidos do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o número de bytes realmente lidos do arquivo. Se não for possível ler mais bytes, o valor de retorno será 0. Se houver um erro, o valor de retorno será 1.

## <a name="remarks"></a>Comentários

O procedimento de e/s é responsável por atualizar o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para refletir a nova posição do arquivo após a operação de leitura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

