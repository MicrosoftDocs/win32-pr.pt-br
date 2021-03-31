---
title: Mensagem de MCIWNDM_SENDSTRING (VFW. h)
description: A \_ mensagem SendString MCIWNDM envia um comando MCI no formato de cadeia de caracteres para o dispositivo associado à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SENDSTRING
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644896"
---
# <a name="mciwndm_sendstring-message"></a>\_Mensagem MCIWNDM SendString

A **mensagem \_ SendString MCIWNDM** envia um comando MCI no formato de cadeia de caracteres para o dispositivo associado à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*sz*
</dt> <dd>

Comando de cadeia de caracteres para enviar para o dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O manipulador de mensagens **para \_ SendString MCIWNDM** anexa um alias de dispositivo ao comando MCI que você envia para o dispositivo. Portanto, você não deve usar nenhum alias em um comando MCI que você emite com **MCIWNDM \_ SendString**.

Para obter a cadeia de caracteres de retorno, que contém o resultado do comando, envie a mensagem de [**\_ retorno de MCIWNDM**](mciwndm-returnstring.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Cadeias de caracteres de comando multimídia](multimedia-command-strings.md)
</dt> </dl>

 

 





