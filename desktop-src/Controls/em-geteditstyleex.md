---
title: Mensagem de EM_GETEDITSTYLEEX (RichEdit. h)
description: Recupera os sinalizadores de estilo de edição estendida atuais.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- controles de Windows de mensagem de EM_GETEDITSTYLEEX
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
# <a name="em_geteditstyleex-message"></a>\_Mensagem em GETEDITSTYLEEX

Recupera os sinalizadores de estilo de edição estendida atuais.


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

Retorna os sinalizadores de estilo de edição estendida, que podem incluir um ou mais dos valores a seguir.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HANDLEFRIENDLYURL de SES \_ ex \_**</dt> </dl>  | Exibir links de nome amigável com a mesma cor de texto e sublinhado como links automáticos, desde que a formatação temporária não seja usada ou use a cor automática do texto (padrão: 0).<br/>                                                                       |
| <dl> <dt>**multitoque de SES \_ ex \_**</dt> </dl>         | Habilite o suporte ao toque em rich edit. Isso inclui seleção, posicionamento de cursor e invocação de menu de contexto. Quando esse sinalizador não é definido, o toque é emulado por comandos do mouse, que não usam as especificidades do modo Touch em conta (padrão: 0). <br/>      |
| <dl> <dt>**NOACETATESELECTION de SES \_ ex \_**</dt> </dl> | exibe o texto selecionado usando o texto clássico de seleção de Windows e cores de plano de fundo em vez da cor acetato de segundo plano (padrão: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ ex \_ nomath**</dt> </dl>             | Desabilite a inserção de zonas matemáticas (padrão: 1). Para habilitar a edição e a exibição de matemática, envie a mensagem em [**\_ SETEDITSTYLEEX**](em-seteditstyleex.md) com *wParam* definido como 0 e *lParam* definido como **ses \_ ex \_ nomath**. <br/>                              |
| <dl> <dt>**SES \_ ex \_ notável**</dt> </dl>            | Desabilite a inserção de tabelas. A mensagem em [**\_ InsertTable**](em-inserttable.md) retorna e as tabelas de **\_ falha** e RTF são ignoradas (padrão: 0). <br/>                                                                                                  |
| <dl> <dt>**USESINGLELINE de SES \_ ex \_**</dt> </dl>      | Habilite um controle de várias linhas para agir como um controle de linha única com a capacidade de rolar verticalmente quando a altura da linha única for maior que a altura da janela (padrão: 0). <br/>                                                                   |
| <dl> <dt>**HIDETEMPFORMAT de SES \_**</dt> </dl>         | Oculte a formatação temporária que é criada quando [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) é chamado com **tomApplyTmp**. Por exemplo, essa formatação é usada por verificadores ortográficos para exibir um sublinhado ondulado sob possíveis palavras escritas incorretamente.<br/> |
| <dl> <dt>**USEMOUSEWPARAM de SES \_ ex \_**</dt> </dl>     | Use *wParam* ao manipular a [**mensagem \_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) e não chame [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md)
</dt> </dl>

 

