---
title: Mensagem de EM_SETLIMITTEXT (WinUser. h)
description: EM_SETLIMITTEXT mensagem – define o limite de texto de um controle de edição.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- Controles de EM_SETLIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109744"
---
# <a name="em_setlimittext-message"></a>\_Mensagem em SETLIMITTEXT

Define o limite de texto de um controle de edição. O limite de texto é a quantidade máxima de texto, em **TCHAR** s, que o usuário pode digitar no controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

Para controles de edição e Microsoft Rich Edit 1,0, são usados bytes. Para o Microsoft rich edit 2,0 e posterior, são usados caracteres.

A mensagem em **\_ SETLIMITTEXT** é idêntica à mensagem [**em \_ LIMITTEXT**](em-limittext.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de **TCHAR** s que o usuário pode inserir. Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres. Esse número não inclui o caractere nulo de terminação.

**Controles de edição avançados:** Se esse parâmetro for zero, o tamanho do texto será definido como 64.000 caracteres.

Se esse parâmetro for zero, o tamanho do texto será definido como 0x7FFFFFFE caracteres para controles de edição de linha única ou 1 para controles de edição de várias linhas.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A mensagem em **\_ SETLIMITTEXT** limita apenas o texto que o usuário pode inserir. Ele não afeta nenhum texto que já esteja no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição pela mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) . Se um aplicativo usar a **mensagem \_ SetText do WM** para posicionar mais texto em um controle de edição do que é especificado na mensagem em **\_ SETLIMITTEXT** , o usuário poderá editar todo o conteúdo do controle de edição.

Antes **de \_ SETLIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir em um controle de edição é de 32.767 caracteres.

Para controles de edição de linha única, o limite de texto é 0x7FFFFFFE bytes ou o valor do parâmetro *wParam* , o que for menor. Para controles de edição de várias linhas, esse valor é 1 bytes ou o valor do parâmetro *wParam* , o que for menor.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Use a mensagem [**em \_ EXLIMITTEXT**](em-exlimittext.md) para valores de comprimento de texto maiores que 64.000. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**em \_ GETLIMITTEXT**](em-getlimittext.md)
</dt> </dl>

 

