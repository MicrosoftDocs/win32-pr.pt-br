---
title: Mensagem de CB_GETLBTEXT (WinUser. h)
description: Obtém uma cadeia de caracteres da lista de uma caixa de combinação.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Controles de CB_GETLBTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009361"
---
# <a name="cb_getlbtext-message"></a>\_Mensagem de GETLBTEXT CB

Obtém uma cadeia de caracteres da lista de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da cadeia de caracteres a ser recuperada.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que recebe a cadeia de caracteres. O buffer deve ter espaço suficiente para a cadeia de caracteres e um caractere nulo de terminação. Você pode enviar uma mensagem [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) antes da mensagem **CB \_ GETLBTEXT** para recuperar o comprimento, em **TCHAR** s, da cadeia de caracteres. Se for uma cadeia de caracteres ANSI, esse será o número de bytes, mas se for uma cadeia de caracteres Unicode, esse será o número de personagens.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação. Se *wParam* não especificar um índice válido, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa. Essa mensagem não fornece uma maneira de saber o tamanho do buffer. Se você usar essa mensagem, primeiro chame [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obter o número de caracteres necessários e, em seguida, chame a mensagem para recuperar a cadeia de caracteres. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o buffer apontado por *lParam* receberá os dados associados ao item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETLBTEXTLEN CB**](cb-getlbtextlen.md)
</dt> </dl>

 

 





