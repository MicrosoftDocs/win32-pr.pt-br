---
title: EM_GETEDITSTYLEEX mensagem (Richedit.h)
description: Recupera os sinalizadores de estilo de edição estendidos atuais.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3c011a162bbf0a1822e68be6bd60f662551b3a22ecfca62c64ef8d01a605a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049306"
---
# <a name="em_geteditstyleex-message"></a>Mensagem EM \_ GETEDITSTYLEEX

Recupera os sinalizadores de estilo de edição estendidos atuais.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna os sinalizadores de estilo de edição estendidos, que podem incluir um ou mais dos valores a seguir.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ EX \_ HANDLEFRIENDLYURL**</dt> </dl>  | Exibir links de nome amigável com a mesma cor de texto e sublinhado que links automáticos, desde que a formatação temporária não seja usada ou use a cor automática de texto (padrão: 0).<br/>                                                                       |
| <dl> <dt>**SES \_ EX \_ MULTITOUCH**</dt> </dl>         | Habilita o suporte a toque no Rich Edit. Isso inclui seleção, posicionamento de adição de aro e invocação de menu de contexto. Quando esse sinalizador não está definido, o toque é emulado por comandos do mouse, que não levam em conta as especificações do modo de toque (padrão: 0). <br/>      |
| <dl> <dt>**SES \_ EX \_ NOACETATESELECTION**</dt> </dl> | Exibe o texto selecionado usando o texto Windows de seleção clássica e as cores da tela de fundo em vez da cor do acetate da tela de fundo (padrão: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ EX \_ NOMATH**</dt> </dl>             | Desabilite a inserção de zonas matemáticas (padrão: 1). Para habilitar a edição e a exibição matemática, envie a mensagem [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) com *wParam* definido como 0 e *lParam definido* como **SES EX \_ \_ NOMATH**. <br/>                              |
| <dl> <dt>**SES \_ EX \_ NOTÁVEL**</dt> </dl>            | Desabilite a inserção de tabelas. A [**mensagem EM \_ INSERTTABLE**](em-inserttable.md) retorna **as tabelas E \_ FAIL** e RTF são ignoradas (padrão: 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ EX \_ USESINGLELINE**</dt> </dl>      | Habilita um controle multilinha a agir como um controle de linha única com a capacidade de rolar verticalmente quando a altura da linha única for maior que a altura da janela (padrão: 0). <br/>                                                                   |
| <dl> <dt>**SES \_ HIDETEMPFORMAT**</dt> </dl>         | Ocultar formatação temporária criada quando [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) é chamado com **tomApplyTmp.** Por exemplo, essa formatação é usada por verificadores ort eletrônicos para exibir um sublinhado deslinhado em palavras possivelmente escritas incorretamente.<br/> |
| <dl> <dt>**SES \_ EX \_ USEMOUSEWPARAM**</dt> </dl>     | Use *wParam ao* manipular a [**mensagem WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e não chame [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)
</dt> </dl>

 

