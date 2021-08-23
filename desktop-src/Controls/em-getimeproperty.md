---
title: EM_GETIMEPROPERTY mensagem (Richedit.h)
description: Recupera a propriedade e os recursos do IME (Editor de Método de Entrada) associado à localidade de entrada atual.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY controles de Windows mensagem
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
ms.openlocfilehash: 3b96ad255d9d68cc76869b6f9163aedf549da19ff0c3ddba756f8da42267135c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541106"
---
# <a name="em_getimeproperty-message"></a>Mensagem \_ EM GETIMEPROPERTY

Recupera a propriedade e os recursos do IME (Editor de Método de Entrada) associado à localidade de entrada atual.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o tipo de informações de propriedade a recuperar. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**PROPRIEDADE \_ IGP**</dt> </dl>                | Informações de propriedade.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**CONVERSÃO de IGP \_**</dt> </dl>          | Funcionalidades de conversão. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**IGP \_ SENTENCE**</dt> </dl>                | Funcionalidades de modo de frase. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**IGP \_ UI**</dt> </dl>                                  | Funcionalidades de interface do usuário. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | Recursos de cadeia de caracteres de composição. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP \_ SELECT**</dt> </dl>                      | Recursos de herança de seleção. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**GETIMEVERSION de IGP \_**</dt> </dl> | Recupera o número de versão do sistema para o qual o IME especificado foi criado. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a propriedade ou o valor da funcionalidade, dependendo do valor do *parâmetro lParam.* Para obter mais informações, consulte Comentários.

## <a name="remarks"></a>Comentários

Se *wParam* for \_ IGP PROPERTY, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ PROP \_ AT \_ CARET                | Se definido, a janela de conversão está na posição do achamado. Se estiver limpa, a janela será próxima à posição do achamado.                                                                                                                                                                  |
| IME \_ PROP \_ SPECIAL \_ UI              | Se definido, o IME terá uma interface do usuário não padrão. O aplicativo não deve desenhar na janela do IME.                                                                                                                                                                  |
| IME \_ PROP \_ CANDLIST \_ A PARTIR DE \_ \_ 1 | Se definido, as cadeias de caracteres na lista de candidatos serão numeradas começando em 1. Se estiver claro, as cadeias de caracteres começarão em zero.                                                                                                                                                                |
| IME \_ PROP \_ UNICODE                  | Se definido, o IME será exibido como um UnicodeIME. O sistema e o IME se comunicarão por meio da interface UnicodeIME. Se estiver claro, o IME usará a interface ANSI para se comunicar com o sistema.                                                                    |
| IME \_ PROP \_ COMPLETE \_ ON \_ UNSELECT   | Se definido, a janela de conversão está na posição do achamado. Se estiver limpa, a janela será próxima à posição do achamado.                                                                                                                                                                  |
| IME \_ PROP \_ ACCEPT \_ WIDE \_ VKEY       | Se definido, o IME processa o Unicode injetado que veio da [**função SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) usando o PACOTE da VK. \_ Se estiver claro, o IME poderá não processar o Unicode injetado e o Unicode injetado poderá ser enviado diretamente ao aplicativo. |



 

Se *wParam for* IGP \_ UI, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|-----------------|-------------------------------------------------------------------------------------------------------|
| CAP \_ \_ 2700 da interface do usuário   | Dá suporte a valores de escape de texto de 0 ou 2700. Para obter mais informações, **consulte lfEscapement**.             |
| LIMITE DE \_ INTERFACE DO \_ USUÁRIO ROT90  | Dá suporte a valores de escape de texto de 0, 900, 1800 ou 2700. Para obter mais informações, **consulte lfEscapement**. |
| ROTANY \_ DE LIMITE DE INTERFACE DO \_ USUÁRIO | Dá suporte a qualquer valor de escape de texto. Para obter mais informações, **consulte lfEscapement**.                       |



 

Se *wParam* for IGP \_ SETCOMPSTR, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS \_ CAP \_ COMPSTR            | Pode criar a cadeia de caracteres de composição chamando [**a função ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) com o valor SETSTR do \_ SCS.                                                      |
| MAKEREAD DE LIMITE DO SCS \_ \_           | Pode criar a cadeia de caracteres de leitura da cadeia de caracteres de composição correspondente ao usar a [**função ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) com SCS SETSTR e \_ sem definir *lpRead*. |
| SCS \_ CAP \_ SETRECONVERTSTRING | Esse IME pode dar suporte à reconversão. Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) para fazer a reconversão.                                                                             |



 

Se *wParam* for IGP \_ SELECT, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|-----------------------|------------------------------------------------------|
| SELECT \_ CAP \_ CONVMODE | Herda o modo de conversão quando um novo IME é selecionado. |
| SELECT \_ CAP \_ SENTENCE | Herda o modo de frase quando um novo IME é selecionado.   |



 

Se *wParam* for IGP \_ GETIMEVERSION, ele retornará um ou mais dos valores a seguir.



| Requisito | Valor |
|--------------|---------------------------------------------|
| IMEVER \_ 0310 | O IME foi criado para Windows 3.1.        |
| IMEVER \_ 0400 | O IME foi criado para Windows 95 ou posterior |



 

Essa mensagem é semelhante a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), exceto que ela usa a localidade de entrada atual. O aplicativo deve chamar [**EM \_ ISIME antes**](em-isime.md) de chamar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

