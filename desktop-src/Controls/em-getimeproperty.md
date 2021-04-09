---
title: Mensagem de EM_GETIMEPROPERTY (RichEdit. h)
description: Recupera a propriedade e os recursos do IME (editor de método de entrada) associado à localidade de entrada atual.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Controles de EM_GETIMEPROPERTY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086037"
---
# <a name="em_getimeproperty-message"></a>\_Mensagem em GETIMEPROPERTY

Recupera a propriedade e os recursos do IME (editor de método de entrada) associado à localidade de entrada atual.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o tipo de informações de propriedade a serem recuperadas. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**\_Propriedade IGP**</dt> </dl>                | Informações de propriedade.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**conversão de IGP \_**</dt> </dl>          | Recursos de conversão. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**sentença de IGP \_**</dt> </dl>                | Recursos do modo de sentença. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**\_interface do usuário do IGP**</dt> </dl>                                  | Recursos da interface do usuário. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**SETCOMPSTR de IGP \_**</dt> </dl>          | Funcionalidades de cadeia de caracteres de composição. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**seleção de IGP \_**</dt> </dl>                      | Funcionalidades de herança de seleção. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**GETIMEVERSION de IGP \_**</dt> </dl> | Recupera o número de versão do sistema para o qual o IME especificado foi criado. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a propriedade ou o valor de funcionalidade, dependendo do valor do parâmetro *lParam* . Para obter mais informações, consulte Comentários.

## <a name="remarks"></a>Comentários

Se *wParam* for \_ a propriedade IGP, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_prop IME \_ no \_ cursor                | Se definido, a janela de conversão estará na posição do cursor. Se estiver claro, a janela estará perto da posição do cursor.                                                                                                                                                                  |
| \_ \_ IU especial de prop IME \_              | Se definido, o IME tem uma interface do usuário não padrão. O aplicativo não deve desenhar na janela do IME.                                                                                                                                                                  |
| O IME \_ prop \_ CANDLIST \_ começa \_ em \_ 1 | Se definido, as cadeias de caracteres na lista de candidatos serão numeradas a partir de 1. Se claro, as cadeias de caracteres começam em zero.                                                                                                                                                                |
| \_Unicode prop do IME \_                  | Se definido, o IME será exibido como um UnicodeIME. O sistema e o IME se comunicarão por meio da interface UnicodeIME. Se claro, o IME usará a interface ANSI para se comunicar com o sistema.                                                                    |
| \_prop IME \_ concluído \_ ao \_ desmarcar   | Se definido, a janela de conversão estará na posição do cursor. Se estiver claro, a janela estará perto da posição do cursor.                                                                                                                                                                  |
| a \_ prop do IME \_ aceita \_ Wide \_ VKEY       | Se definido, o IME processará o Unicode injetado que veio da função [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) usando o \_ pacote VK. Se estiver claro, o IME poderá não processar o Unicode injetado, e o Unicode injetado poderá ser enviado diretamente ao aplicativo. |



 

Se *wParam* for \_ a interface do usuário do IGP, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|-----------------|-------------------------------------------------------------------------------------------------------|
| Limite de interface do usuário \_ \_ 2700   | Dá suporte a valores de escape de texto 0 ou 2700. Para obter mais informações, consulte **lfEscapement**.             |
| \_ROT90 Cap da interface do usuário \_  | Dá suporte a valores de escape de texto de 0, 900, 1800 ou 2700. Para obter mais informações, consulte **lfEscapement**. |
| \_ROTANY Cap da interface do usuário \_ | Dá suporte a qualquer valor de escape de texto. Para obter mais informações, consulte **lfEscapement**.                       |



 

Se *wParam* for \_ o IGP SETCOMPSTR, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_COMPSTR Cap do SCS \_            | Pode criar a cadeia de caracteres de composição chamando a função [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) com o valor de SETSTR do SCS \_ .                                                      |
| \_MAKEREAD Cap do SCS \_           | Pode criar a cadeia de caracteres de leitura da cadeia de caracteres de composição correspondente ao usar a função [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) com o SCS \_ SETSTR e sem definir *lpRead*. |
| \_SETRECONVERTSTRING Cap do SCS \_ | Este IME pode dar suporte à reconversão. Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) para fazer a reconversão.                                                                             |



 

Se *wParam* for \_ o IGP Select, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|-----------------------|------------------------------------------------------|
| Selecione \_ \_ arconvmode de Cap | Herda o modo de conversão quando um novo IME é selecionado. |
| SELECIONAR \_ frase de extremidade \_ | Herda o modo de frase quando um novo IME é selecionado.   |



 

Se *wParam* for \_ o IGP GETIMEVERSION, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|--------------|---------------------------------------------|
| Nunca \_ 0310 | O IME foi criado para o Windows 3,1.        |
| Nunca \_ 0400 | O IME foi criado para o Windows 95 ou posterior |



 

Essa mensagem é semelhante a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), exceto pelo fato de que ela usa a localidade de entrada atual. O aplicativo deve chamar [**em \_ ISIME**](em-isime.md) antes de chamar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ ISIME**](em-isime.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

