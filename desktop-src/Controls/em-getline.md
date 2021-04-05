---
title: Mensagem de EM_GETLINE (WinUser. h)
description: Copia uma linha de texto de um controle de edição e a coloca em um buffer especificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controles de EM_GETLINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918066"
---
# <a name="em_getline-message-winuserh"></a>Mensagem de EM_GETLINE (WinUser. h)

Copia uma linha de texto de um controle de edição e a coloca em um buffer especificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da linha a ser recuperada de um controle de edição de várias linhas. Um valor de zero Especifica a linha superior. Esse parâmetro é ignorado por um controle de edição de linha única.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que recebe uma cópia da linha. Antes de enviar a mensagem, defina a primeira palavra desse buffer com o tamanho, em **TCHAR** s, do buffer. Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres. O tamanho na primeira palavra é substituído pela linha copiada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de **TCHAR** s copiados. O valor de retorno será zero se o número de linha especificado pelo parâmetro *wParam* for maior que o número de linhas no controle de edição.

## <a name="remarks"></a>Comentários

**Controles de edição:** A linha copiada não contém um caractere nulo de terminação.

**Controles de edição avançados:** Com suporte no Microsoft Rich Edit 1,0 e posterior. A linha copiada não contém um caractere nulo de terminação, a menos que nenhum texto tenha sido copiado. Se nenhum texto for copiado, a mensagem colocará um caractere nulo no início do buffer. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Editar \_ getline**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

