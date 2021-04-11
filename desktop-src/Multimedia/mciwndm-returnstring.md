---
title: Mensagem de MCIWNDM_RETURNSTRING (VFW. h)
description: A \_ mensagem returnstring MCIWNDM recupera a resposta para o comando de cadeia de caracteres MCI mais recente enviado para um dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- Multimídia do Windows de mensagem MCIWNDM_RETURNSTRING
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009340"
---
# <a name="mciwndm_returnstring-message"></a>Mensagem de retorno de MCIWNDM \_

A **mensagem \_ returnstring MCIWNDM** recupera a resposta para o comando de cadeia de caracteres MCI mais recente enviado para um dispositivo MCI. As informações na resposta são fornecidas como uma cadeia de caracteres terminada em nulo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .


```C++
MCIWNDM_RETURNSTRING 
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

Ponteiro para um buffer definido pelo aplicativo para conter a cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à cadeia de caracteres MCI.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres terminada em nulo for maior que o buffer, a cadeia de caracteres será truncada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





