---
title: Mensagem de EM_GETFILELINE (CommCtrl. h)
description: Copia uma linha de texto de um controle de edição, independentemente de como as linhas são exibidas na tela e as coloca em um buffer especificado.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- controles de Windows de mensagem de EM_GETFILELINE
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 470c437280b279f56c3dcc8b45de93cf3f792afc5053b7e312b2c19c7ffcec8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049216"
---
# <a name="em_getfileline-message-commctrlh"></a>Mensagem de EM_GETFILELINE (CommCtrl. h)

Copia uma linha de texto de um controle de edição, independentemente de como as linhas são exibidas na tela e as coloca em um buffer especificado.

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

## <a name="return-value"></a>Valor retornado

O valor de retorno é o número de **TCHAR** s copiados. O valor de retorno será zero se o número de linha especificado pelo parâmetro *wParam* for maior que o número de linhas no controle de edição.

## <a name="remarks"></a>Comentários

A linha copiada não contém um caractere nulo de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, 1809 \[ aplicativos de área de trabalho apenas\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2019\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Editar \_ GetFile**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

