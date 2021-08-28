---
title: Estilos de caixa de combinação (CommCtrl.h)
description: Para criar uma caixa de combinação usando a função CreateWindow ou CreateWindowEx, especifique a classe COMBOBOX, as constantes de estilo de janela apropriadas e uma combinação dos seguintes estilos de caixa de combinação.
ms.assetid: 4dc347b2-7da7-4aa0-b61f-781acf652d84
topic_type:
- apiref
api_name:
- CBS_AUTOHSCROLL
- CBS_DISABLENOSCROLL
- CBS_DROPDOWN
- CBS_DROPDOWNLIST
- CBS_HASSTRINGS
- CBS_LOWERCASE
- CBS_NOINTEGRALHEIGHT
- CBS_OEMCONVERT
- CBS_OWNERDRAWFIXED
- CBS_OWNERDRAWVARIABLE
- CBS_SIMPLE
- CBS_SORT
- CBS_UPPERCASE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652a6392cf8ce50f01efa215e8d6472d1fd1ff344b35fb36d72f0e5dc3c48c68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968496"
---
# <a name="combo-box-styles"></a>Estilos de caixa de combinação

Para criar uma caixa de combinação usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especifique a classe COMBOBOX, as constantes de estilo de janela apropriadas e uma combinação dos seguintes estilos de caixa de combinação.



| Constante                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**CBS \_ AUTOHSCROLL**</dt> </dl>                   | Rola automaticamente o texto em um controle de edição para a direita quando o usuário digita um caractere no final da linha. Se esse estilo não for definido, somente o texto que se ajusta ao limite retangular será permitido.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**CBS \_ DISABLENOSCROLL**</dt> </dl>       | Mostra uma barra de rolagem vertical desabilitada na caixa de listagem quando a caixa não contém itens suficientes para rolar. Sem esse estilo, a barra de rolagem fica oculta quando a caixa de listagem não contém itens suficientes.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**MENU SUSPENSO DO CBS \_**</dt> </dl>                            | Semelhante ao CBS SIMPLE, exceto que a caixa de listagem não é exibida, a menos que o usuário selecione um \_ ícone ao lado do controle de edição.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**CBS \_ DROPDOWNLIST**</dt> </dl>                | Semelhante ao CBS DROPDOWN, exceto que o controle de edição é substituído por um item de texto estático que exibe a seleção \_ atual na caixa de listagem.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**CBS \_ HASSTRINGS**</dt> </dl>                      | Especifica que uma caixa de combinação desenhada pelo proprietário contém itens que consistem em cadeias de caracteres. A caixa de combinação mantém a memória e o endereço das cadeias de caracteres para que o aplicativo possa usar a mensagem [**\_ CB GETLBTEXT**](cb-getlbtext.md) para recuperar o texto de um item específico.<br/> Para problemas de acessibilidade, consulte [Expondo itens Owner-Drawn caixa de combinação](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**CBS \_ LOWERCASE**</dt> </dl>                         | Converte em letras minúsculas todo o texto no campo de seleção e na lista. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**CBS \_ NOINTEGRALHEIGHT**</dt> </dl>    | Especifica que o tamanho da caixa de combinação é exatamente o tamanho especificado pelo aplicativo quando ele criou a caixa de combinação. Normalmente, o sistema tamanhos de uma caixa de combinação para que ele não exibe itens parciais.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**CBS \_ OEMCONVERT**</dt> </dl>                      | Converte o texto inserido no controle de edição da caixa de combinação Windows caracteres definido para o conjunto de caracteres OEM e, em seguida, de volta para o conjunto Windows caracteres. Isso garante a conversão de caracteres adequada quando o aplicativo chama a função [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) para converter uma cadeia Windows cadeia de caracteres na caixa de combinação em caracteres OEM. Esse estilo é mais útil para caixas de combinação que contêm nomes de arquivo e se aplica somente a caixas de combinação criadas com o estilo CBS SIMPLE ou \_ CBS \_ DROPDOWN.<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**CBS \_ OWNERDRAWFIXED**</dt> </dl>          | Especifica que o proprietário da caixa de listagem é responsável por desenhar seu conteúdo e que os itens na caixa de listagem têm a mesma altura. A janela proprietário recebe uma mensagem [**WM \_ MEASUREITEM**](wm-measureitem.md) quando a caixa de combinação é criada e uma mensagem [**WM \_ DRAWITEM**](wm-drawitem.md) quando um aspecto visual da caixa de combinação é alterado.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**CBS \_ OWNERDRAWVARIABLE**</dt> </dl> | Especifica que o proprietário da caixa de listagem é responsável por desenhar seu conteúdo e que os itens na caixa de listagem são variáveis de altura. A janela proprietário recebe uma mensagem [**WM \_ MEASUREITEM**](wm-measureitem.md) para cada item na caixa de combinação quando você cria a caixa de combinação e uma mensagem [**WM \_ DRAWITEM**](wm-drawitem.md) quando um aspecto visual da caixa de combinação é alterado.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ SIMPLE**</dt> </dl>                                  | Exibe a caixa de listagem o tempo todo. A seleção atual na caixa de listagem é exibida no controle de edição.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**CBS \_ SORT**</dt> </dl>                                        | Classifica automaticamente as cadeias de caracteres adicionadas à caixa de listagem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**CBS \_ UPPERCASE**</dt> </dl>                         | Converte em letras maiúsculas todo o texto no campo de seleção e na lista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

