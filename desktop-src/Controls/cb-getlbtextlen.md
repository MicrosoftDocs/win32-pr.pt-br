---
title: Mensagem de CB_GETLBTEXTLEN (WinUser. h)
description: Obtém o comprimento, em caracteres, de uma cadeia de caracteres na lista de uma caixa de combinação.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Controles de CB_GETLBTEXTLEN de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918434"
---
# <a name="cb_getlbtextlen-message"></a>\_Mensagem de GETLBTEXTLEN CB

Obtém o comprimento, em caracteres, de uma cadeia de caracteres na lista de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da cadeia de caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação. Se uma cadeia de caracteres ANSI for o número de bytes e se for uma cadeia de caracteres Unicode, esse será o número de caracteres. Em determinadas condições, esse valor pode ser, na verdade, maior que o comprimento do texto. Para obter mais informações, consulte a seção Comentários.

Se o parâmetro *wParam* não especificar um índice válido, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

Em determinadas condições, o valor de retorno é maior do que o comprimento real do texto. Isso ocorre com determinadas misturas de ANSI e Unicode e é devido ao sistema operacional permitir a possível existência de caracteres de conjunto de caracteres de dois bytes (DBCS) dentro do texto. O valor de retorno, no entanto, sempre será pelo menos tão grande quanto o comprimento real do texto; Portanto, você sempre pode usá-lo para guiar a alocação do buffer. Esse comportamento pode ocorrer quando um aplicativo usa funções ANSI e caixas de diálogo comuns, que usam Unicode.

Para obter o comprimento exato do texto, use as mensagens [**do \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou a função [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETLBTEXT CB**](cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETtext**](lb-gettext.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

