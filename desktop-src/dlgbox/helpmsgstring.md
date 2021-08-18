---
title: Mensagem de HELPMSGSTRING (Commdlg. h)
description: Uma caixa de diálogo comum envia a mensagem registrada HELPMSGSTRING para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão ajuda.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Caixas de diálogo de mensagem HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8a446164bb7ae51d36d1a89219f6c3b84eff74b9af3a40c2121b3bd205a581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741736"
---
# <a name="helpmsgstring-message"></a>Mensagem HELPMSGSTRING

Uma caixa de diálogo comum envia a mensagem registrada **HELPMSGSTRING** para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão **ajuda** .


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a caixa de diálogo comum.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a estrutura de inicialização da caixa de diálogo comum. Essa estrutura pode ser uma estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) ou [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Você deve especificar a constante **HELPMSGSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.

Quando você criar a caixa de diálogo, use o membro **hwndOwner** da estrutura de inicialização para identificar a janela para receber mensagens **HELPMSGSTRING** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HELPMSGSTRINGW** (Unicode) e **HELPMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CDN \_ AJUDA**](cdn-help.md)
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**DA OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

