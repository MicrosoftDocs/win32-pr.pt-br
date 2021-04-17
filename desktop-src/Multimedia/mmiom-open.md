---
title: Mensagem de MMIOM_OPEN (mmsystem. h)
description: A \_ mensagem MMIOM Open é enviada a um procedimento de e/s pela função mmioOpen para solicitar que um arquivo seja aberto ou excluído.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- Multimídia do Windows de mensagem MMIOM_OPEN
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748129"
---
# <a name="mmiom_open-message"></a>MMIOM \_ Abrir mensagem

A mensagem **MMIOM \_ Open** é enviada a um procedimento de e/s pela função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para solicitar que um arquivo seja aberto ou excluído.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo a ser aberto.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna MMSYSERR \_ NOERROR se for bem-sucedido ou um erro de outra forma. Os possíveis valores de erro incluem o seguinte:



| Requisito | Valor |
|--------------------|---------------------------------------------|
| MMIOM \_ CANNOTOPEN  | Não foi possível abrir o arquivo.               |
| \_OUTOFMEMORY MMIOM | Não há memória suficiente para executar a operação. |



 

## <a name="remarks"></a>Comentários

O membro **dwFlags** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contém sinalizadores passados para a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .

O membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) é inicializado como zero. Se esse valor estiver incorreto, o procedimento de e/s deverá corrigi-lo.

Se o aplicativo passasse uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), o valor de retorno será retornado no membro **wErrorRet** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

