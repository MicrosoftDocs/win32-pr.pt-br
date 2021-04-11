---
title: Mensagem de EM_LIMITTEXT (WinUser. h)
description: Define o limite de texto de um controle de edição.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- Controles de EM_LIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454943"
---
# <a name="em_limittext-message"></a>\_Mensagem em LIMITTEXT

Define o limite de texto de um controle de edição. O limite de texto é a quantidade máxima de texto, em **TCHAR** s, que o usuário pode digitar no controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

Para controles de edição e Microsoft Rich Edit 1,0, são usados bytes. Para o Microsoft rich edit 2,0 e posterior, são usados caracteres.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de **TCHAR** s que o usuário pode inserir. Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres. Esse número não inclui o caractere nulo de terminação.

**Controles de edição avançados:** Se esse parâmetro for zero, o tamanho do texto será definido como 64.000 caracteres.

Se esse parâmetro for zero, o tamanho do texto será definido como 0x7FFFFFFE caracteres para controles de edição de linha única ou-1 para controles de edição de várias linhas.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A mensagem em **\_ LIMITTEXT** limita apenas o texto que o usuário pode inserir. Ele não afeta nenhum texto que já esteja no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição pela mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) . Se um aplicativo usar a **mensagem \_ SetText do WM** para posicionar mais texto em um controle de edição do que é especificado na mensagem em **\_ LIMITTEXT** , o usuário poderá editar todo o conteúdo do controle de edição.

Antes **de \_ LIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir em um controle de edição é de 32.767 caracteres.

Para controles de edição de linha única, o limite de texto é 0x7FFFFFFE bytes ou o valor do parâmetro *wParam* , o que for menor. Para controles de edição de várias linhas, esse valor é-1 byte ou o valor do parâmetro *wParam* , o que for menor.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Use a mensagem [**em \_ EXLIMITTEXT**](em-exlimittext.md) para valores de comprimento de texto maiores que 64.000. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ EXLIMITTEXT**](em-exlimittext.md)
</dt> <dt>

[**Editar \_ LimitText**](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

