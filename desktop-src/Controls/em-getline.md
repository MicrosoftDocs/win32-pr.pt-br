---
title: EM_GETLINE mensagem (Winuser.h)
description: Copia uma linha de texto de um controle de edição e a coloca em um buffer especificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE controles de Windows mensagem
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
ms.openlocfilehash: f4398fa27acf6d70d100c4aa98a1e06c2d6685b7a06cf6effc7e0666bbd6a1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006689"
---
# <a name="em_getline-message-winuserh"></a>EM_GETLINE mensagem (Winuser.h)

Copia uma linha de texto de um controle de edição e a coloca em um buffer especificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero da linha a ser recuperado de um controle de edição multilinha. Um valor de zero especifica a linha mais alta. Esse parâmetro é ignorado por um controle de edição de linha única.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que recebe uma cópia da linha. Antes de enviar a mensagem, de definir a primeira palavra desse buffer para o tamanho, em **TCHAR** s, do buffer. Para texto ANSI, esse é o número de bytes; para texto Unicode, esse é o número de caracteres. O tamanho na primeira palavra é substituído pela linha copiada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o número de **TCHAR** copiados. O valor de retorno será zero se o número de linha especificado pelo *parâmetro wParam* for maior que o número de linhas no controle de edição.

## <a name="remarks"></a>Comentários

**Editar controles:** A linha copiada não contém um caractere nulo de terminação.

**Controles de edição rich:** Com suporte no Microsoft Rich Edit 1.0 e posterior. A linha copiada não contém um caractere nulo de terminação, a menos que nenhum texto tenha sido copiado. Se nenhum texto foi copiado, a mensagem coloca um caractere nulo no início do buffer. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLine**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

