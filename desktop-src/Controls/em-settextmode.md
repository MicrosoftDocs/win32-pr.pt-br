---
title: EM_SETTEXTMODE mensagem (Richedit.h)
description: Define o modo de texto ou o nível de desfazer de um controle de edição rico. A mensagem falhará se o controle contiver qualquer texto.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE controles de Windows mensagem
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
ms.openlocfilehash: 0ea489dcdb60908cac8600188d40b9aae4b7e3e531c713094bb180e84ee24bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672365"
---
# <a name="em_settextmode-message"></a>Mensagem EM \_ SETTEXTMODE

Define o modo de texto ou o nível de desfazer de um controle de edição rico. A mensagem falhará se o controle contiver qualquer texto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais valores do tipo [**de enumeração TEXTMODE.**](/windows/win32/api/richedit/ne-richedit-textmode) Os valores especificam as novas configurações para o modo de texto do controle e os parâmetros de nível de desfazer.

Especifique um dos valores a seguir para definir o parâmetro de modo de texto. Se você não especificar um valor de modo de texto, o modo de texto permanecerá em sua configuração atual. 

| Valor                                          | Significado                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ PLAINTEXT**](/windows/win32/api/richedit/ne-richedit-textmode) | Indica o modo de texto sem-texto, no qual o controle é semelhante a um controle de edição padrão. Para obter mais informações sobre o modo de texto sem-texto, consulte a seção Comentários a seguir. |
| [**TM \_ RICHTEXT**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indica o modo de rich text, no qual o controle tem a funcionalidade de edição avançada padrão. O modo de rich text é a configuração padrão.                                           |



 

Especifique um dos valores a seguir para definir o parâmetro de nível de desfazer. Se você não especificar um valor de nível de desfazer, o nível de desfazer permanecerá em sua configuração atual. 

| Valor                                                      | Significado                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | O controle permite que o usuário desfaça apenas a última ação que pode ser desfeita.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | O controle dá suporte a várias operações de desfazer. Essa é a configuração padrão. Use a [**mensagem EM \_ SETUNDOLIMIT**](em-setundolimit.md) para definir o número máximo de ações de desfazer. |



 

Especifique um dos valores a seguir para definir o parâmetro de página de código. Se você não especificar um valor de página de código, a página de código permanecerá em sua configuração atual. 

| Valor                                                    | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | O controle só permite o teclado em inglês e um teclado correspondentes ao conjunto de caracteres padrão. Por exemplo, você pode ter grego e inglês. Observe que isso impede que o texto Unicode entre no controle . Por exemplo, use esse valor se um controle Rich Edit deve ser restrito ao texto ANSI. |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | O controle permite várias páginas de código e texto Unicode no controle . Essa é a configuração padrão.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será zero.

Se a mensagem falhar, o valor de retorno será um valor não zero.

## <a name="remarks"></a>Comentários

No modo de rich text, um controle de edição avançada tem a funcionalidade de edição avançada padrão. No entanto, no modo de texto sem-texto, o controle é semelhante a um controle de edição padrão:

-   O texto em um controle de texto sem formatação pode ter apenas um formato (como Negrito, 10pt Arial).
-   O usuário não pode colar formatos de texto rich text, como RTF (Rich Text Format) ou objetos inseridos em um controle de texto sem formatação.
-   Controles de modo de rich text sempre têm um marcador de fim de documento padrão ou retorno de carro para formatar parágrafos. Os controles de texto sem-texto, por outro lado, não precisam do marcador padrão de fim do documento, portanto, ele é omitido.

O controle não deve conter texto quando recebe a **mensagem EM \_ SETTEXTMODE.** Para garantir que não haja texto, envie uma mensagem [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) com uma cadeia de caracteres vazia ("").

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETTEXTMODE**](em-gettextmode.md)
</dt> <dt>

[**EM \_ SETUNDOLIMIT**](em-setundolimit.md)
</dt> <dt>

[**Textmode**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

