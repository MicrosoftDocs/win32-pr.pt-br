---
title: Mensagem de EM_SETTEXTMODE (RichEdit. h)
description: Define o modo de texto ou o nível de desfazer de um controle de edição rico. A mensagem falhará se o controle contiver qualquer texto.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Controles de EM_SETTEXTMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918616"
---
# <a name="em_settextmode-message"></a>\_Mensagem em SETtextmode

Define o modo de texto ou o nível de desfazer de um controle de edição rico. A mensagem falhará se o controle contiver qualquer texto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais valores do tipo de enumeração [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) . Os valores especificam as novas configurações para o modo de texto do controle e os parâmetros de nível de desfazer.

Especifique um dos valores a seguir para definir o parâmetro de modo de texto. Se você não especificar um valor de modo de texto, o modo de texto permanecerá em sua configuração atual. 

| Valor                                          | Significado                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ sem formatação**](/windows/win32/api/richedit/ne-richedit-textmode) | Indica o modo de texto sem formatação, no qual o controle é semelhante a um controle de edição padrão. Para obter mais informações sobre o modo de texto sem formatação, consulte a seção de comentários a seguir. |
| [**RICHTEXT de TM \_**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indica o modo de Rich Text, no qual o controle tem a funcionalidade de edição avançada padrão. O modo de Rich Text é a configuração padrão.                                           |



 

Especifique um dos valores a seguir para definir o parâmetro de nível de desfazer. Se você não especificar um valor de nível de desfazer, o nível de desfazer permanecerá em sua configuração atual. 

| Valor                                                      | Significado                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | O controle permite que o usuário desfaça apenas a última ação que pode ser desfeita.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | O controle dá suporte a várias operações de desfazer. Essa é a configuração padrão. Use a mensagem em [**\_ SETUNDOLIMIT**](em-setundolimit.md) para definir o número máximo de ações de desfazer. |



 

Especifique um dos valores a seguir para definir o parâmetro de página de código. Se você não especificar um valor de página de código, a página de código permanecerá em sua configuração atual. 

| Valor                                                    | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | O controle só permite o teclado em inglês e um teclado correspondente ao conjunto de caracteres padrão. Por exemplo, você pode ter grego e inglês. Observe que isso impede que o texto Unicode entre no controle. Por exemplo, use esse valor se um controle de edição rico precisar ser restrito ao texto ANSI. |
| [**TM \_ MULTIcodepage**](/windows/win32/api/richedit/ne-richedit-textmode)   | O controle permite várias páginas de código e texto Unicode no controle. Essa é a configuração padrão.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, o valor de retorno será zero.

Se a mensagem falhar, o valor de retorno será um valor diferente de zero.

## <a name="remarks"></a>Comentários

No modo Rich Text, um controle rich edit tem funcionalidade de edição avançada padrão. No entanto, no modo de texto sem formatação, o controle é semelhante a um controle de edição padrão:

-   O texto em um controle de texto sem formatação pode ter apenas um formato (como negrito, 10pt Arial).
-   O usuário não pode colar formatos de Rich Text, como Rich Text Format (RTF) ou objetos incorporados em um controle de texto sem formatação.
-   Controles de modo de Rich Text sempre têm um marcador de fim de documento padrão ou retorno de carro, para formatar parágrafos. Os controles de texto sem formatação, por outro lado, não precisam do marcador padrão de fim de documento, portanto, ele é omitido.

O controle não deve conter nenhum texto quando receber a mensagem em **\_ settextmode** . Para garantir que não haja texto, envie uma mensagem de [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) com uma cadeia de caracteres vazia ("").

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETtextmode**](em-gettextmode.md)
</dt> <dt>

[**em \_ SETUNDOLIMIT**](em-setundolimit.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

