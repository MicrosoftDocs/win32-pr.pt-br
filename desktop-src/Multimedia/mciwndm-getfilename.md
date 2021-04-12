---
title: Mensagem de MCIWNDM_GETFILENAME (VFW. h)
description: A \_ mensagem MCIWNDM GETFILENAME recupera o nome de arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETFILENAME
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499257"
---
# <a name="mciwndm_getfilename-message"></a>\_Mensagem MCIWNDM GETFILENAME

A mensagem **MCIWNDM \_ GETFILENAME** recupera o nome de arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo para retornar o nome do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou 1 caso contrário.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres terminada em nulo que contém o nome do arquivo for maior do que o buffer, MCIWnd truncará o nome do arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





