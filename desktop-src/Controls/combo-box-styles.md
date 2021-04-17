---
title: Estilos de caixa de combinação (CommCtrl. h)
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
ms.openlocfilehash: 74f531b93725f3aa92778a42bae3dd3fd972534e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752605"
---
# <a name="combo-box-styles"></a>Estilos de caixa de combinação

Para criar uma caixa de combinação usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique a classe ComboBox, as constantes de estilo de janela apropriadas e uma combinação dos seguintes estilos de caixa de combinação.



| Constante                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**\_AUTOHSCROLL CBS**</dt> </dl>                   | Rola automaticamente o texto em um controle de edição para a direita quando o usuário digita um caractere no final da linha. Se esse estilo não for definido, somente o texto que couber no limite Retangular será permitido.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL CBS**</dt> </dl>       | Mostra uma barra de rolagem vertical desabilitada na caixa de listagem quando a caixa não contém itens suficientes para rolar. Sem esse estilo, a barra de rolagem fica oculta quando a caixa de listagem não contém itens suficientes.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**\_lista suspensa CBS**</dt> </dl>                            | Semelhante ao CBS \_ simples, exceto que a caixa de listagem não é exibida, a menos que o usuário selecione um ícone ao lado do controle de edição.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**DROPDOWNLIST do CBS \_**</dt> </dl>                | Semelhante à \_ lista suspensa CBS, exceto pelo fato de que o controle de edição é substituído por um item de texto estático que exibe a seleção atual na caixa de listagem.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**\_HASSTRINGS CBS**</dt> </dl>                      | Especifica que uma caixa de combinação desenhada pelo proprietário contém itens que consistem em cadeias de caracteres. A caixa de combinação mantém a memória e o endereço das cadeias de caracteres para que o aplicativo possa usar a mensagem [**\_ GETLBTEXT do CB**](cb-getlbtext.md) para recuperar o texto de um determinado item.<br/> Para problemas de acessibilidade, consulte [expondo Owner-Drawn itens da caixa de combinação](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**\_minúsculas do CBS**</dt> </dl>                         | Converte em minúsculas todo o texto no campo de seleção e na lista. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**\_NOINTEGRALHEIGHT CBS**</dt> </dl>    | Especifica que o tamanho da caixa de combinação é exatamente o tamanho especificado pelo aplicativo quando ele criou a caixa de combinação. Normalmente, o sistema dimensiona uma caixa de combinação para que ela não exiba itens parciais.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**\_OEMCONVERT CBS**</dt> </dl>                      | Converte o texto inserido no controle de edição da caixa de combinação do conjunto de caracteres do Windows para o conjunto de caracteres OEM e, em seguida, de volta para o conjunto de caracteres do Windows. Isso garante a conversão adequada de caracteres quando o aplicativo chama a função [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) para converter uma cadeia de caracteres do Windows na caixa de combinação para caracteres OEM. Esse estilo é mais útil para caixas de combinação que contêm nomes de arquivo e aplica-se somente a caixas de combinação criadas com o \_ estilo DROPDOWN simples ou CBS do CBS \_ .<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**\_OwnerDrawFixed CBS**</dt> </dl>          | Especifica que o proprietário da caixa de listagem é responsável por desenhar seu conteúdo e que os itens na caixa de listagem têm a mesma altura. A janela do proprietário recebe uma mensagem do [**WM \_ MEASUREITEM**](wm-measureitem.md) quando a caixa de combinação é criada e uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) quando um aspecto visual da caixa de combinação é alterado.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**\_OwnerDrawVariable CBS**</dt> </dl> | Especifica que o proprietário da caixa de listagem é responsável por desenhar seu conteúdo e que os itens na caixa de listagem são variáveis em altura. A janela do proprietário recebe uma mensagem do [**WM \_ MEASUREITEM**](wm-measureitem.md) para cada item na caixa de combinação quando você cria a caixa de combinação e uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) quando um aspecto visual da caixa de combinação é alterado.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ simples**</dt> </dl>                                  | Exibe a caixa de listagem em todos os momentos. A seleção atual na caixa de listagem é exibida no controle de edição.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**\_classificação CBS**</dt> </dl>                                        | Classifica automaticamente as cadeias de caracteres adicionadas à caixa de listagem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**\_maiúsculas do CBS**</dt> </dl>                         | Converte para todo o texto em maiúsculas no campo de seleção e na lista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

