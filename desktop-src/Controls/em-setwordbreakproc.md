---
title: Mensagem de EM_SETWORDBREAKPROC (WinUser. h)
description: Substitui uma função WordWrap padrão do controle de edição por uma função WordWrap definida pelo aplicativo. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Controles de EM_SETWORDBREAKPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499440"
---
# <a name="em_setwordbreakproc-message"></a>\_Mensagem em SETWORDBREAKPROC

Substitui uma função WordWrap padrão do controle de edição por uma função WordWrap definida pelo aplicativo. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

O endereço da função WordWrap definida pelo aplicativo. Para obter mais informações sobre linhas de quebra, consulte a descrição da função de retorno de chamada [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Uma função WordWrap examina um buffer de texto que contém o texto a ser enviado para a tela, procurando a primeira palavra que não caiba na linha da tela atual. A função WordWrap coloca essa palavra no início da próxima linha na tela.

Uma função WordWrap define o ponto no qual o sistema deve quebrar uma linha de texto para controles de edição de várias linhas, geralmente com um caractere de espaço que separa duas palavras. Um controle de várias linhas ou de edição de linha única pode chamar essa função quando o usuário pressiona as teclas de seta em combinação com a tecla CTRL para mover o cursor para a próxima palavra ou palavra anterior. A função WordWrap padrão quebra uma linha de texto com um caractere de espaço. A função definida pelo aplicativo pode definir o WordWrap para ocorrer em um hífen ou um caractere que não seja o caractere de espaço.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**em \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**em \_ GETWORDBREAKPROC**](em-getwordbreakproc.md)
</dt> </dl>

 

