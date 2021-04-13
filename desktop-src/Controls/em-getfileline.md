---
title: Mensagem de EM_GETFILELINE (CommCtrl. h)
description: Copia uma linha de texto de um controle de edição, independentemente de como as linhas são exibidas na tela e as coloca em um buffer especificado.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controles de EM_GETFILELINE de mensagens do Windows
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
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455547"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de **TCHAR** s copiados. O valor de retorno será zero se o número de linha especificado pelo parâmetro *wParam* for maior que o número de linhas no controle de edição.

## <a name="remarks"></a>Comentários

A linha copiada não contém um caractere nulo de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



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

 

