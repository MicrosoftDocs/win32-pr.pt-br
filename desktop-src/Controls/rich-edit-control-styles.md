---
title: Estilos de controle de edição avançados (WinUser. h)
description: Os estilos de janela a seguir são exclusivos para controles de edição avançados.
ms.assetid: 0f1b3e01-01cb-4b3e-b959-6f32498f0394
topic_type:
- apiref
api_name:
- ES_DISABLENOSCROLL
- ES_EX_NOCALLOLEINIT
- ES_NOIME
- ES_NOOLEDRAGDROP
- ES_SAVESEL
- ES_SELECTIONBAR
- ES_SELFIME
- ES_SUNKEN
- ES_VERTICAL
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620f73beb726eea065d8c8a63a635ff04fdeba37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755423"
---
# <a name="rich-edit-control-styles"></a>Estilos de controle de edição avançados

Os estilos de janela a seguir são exclusivos para controles de edição avançados.



| Constante                                                                                                                                                                         | Descrição                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**ES \_ DISABLENOSCROLL**</dt> </dl>     | Desabilita as barras de rolagem em vez de ocultá-las quando elas não são necessárias.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ ex \_ NOCALLOLEINIT**</dt> </dl> | Impede que o controle chame a função [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) quando criado. Este estilo de janela só é útil em modelos de caixa de diálogo porque [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) não aceita esse estilo.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**Es \_ NOIME**</dt> </dl>                                | Desabilita a operação do IME. Esse estilo está disponível apenas para suporte a idiomas asiáticos.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**ES \_ NOOLEDRAGDROP**</dt> </dl>           | Desabilita o suporte para arrastar e soltar de objetos OLE.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**ES \_ SAVESEL**</dt> </dl>                             | Preserva a seleção quando o controle perde o foco. Por padrão, todo o conteúdo do controle é selecionado quando ele recupera o foco.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**ES \_ SELECTIONBAR**</dt> </dl>              | Adiciona espaço à margem esquerda onde o cursor é alterado para uma seta para a direita, permitindo que o usuário Selecione linhas de texto completas. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**Es \_ SELFIME**</dt> </dl>                          | Direciona o controle de edição rico para permitir que o aplicativo manipule todas as operações do IME. Esse estilo está disponível apenas para suporte a idiomas asiáticos.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES de \_ baixo relevo**</dt> </dl>                                | Exibe o controle com um estilo de borda de baixo e baixo para que o controle de edição rico pareça embutido em sua janela pai. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**\_vertical es**</dt> </dl>                          | Desenha texto e objetos em uma direção vertical. Esse estilo está disponível apenas para suporte a idiomas asiáticos.<br/>                                                                                                                                 |



Os controles de edição avançados também dão suporte aos seguintes estilos de controle de edição.



| Constante                                                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**ES \_ AUTOHSCROLL**</dt> </dl> | Rola automaticamente o texto para a direita em 10 caracteres quando o usuário digita um caractere no final da linha. Quando o usuário pressiona a tecla ENTER, o controle rola todo o texto de volta para a posição zero.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**ES \_ AUTOVSCROLL**</dt> </dl> | Rola automaticamente o texto uma página para cima quando o usuário pressiona a tecla ENTER na última linha.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**\_Centro es**</dt> </dl>                | Centraliza o texto em um controle de linha única ou de edição de várias linhas.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**ES \_ à esquerda**</dt> </dl>                      | Alinha o texto à esquerda.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**s \_ multilinha**</dt> </dl>       | Designa um controle de edição de várias linhas. O padrão é o controle de edição de linha única.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**ES \_ NOHIDESEL**</dt> </dl>       | Nega o comportamento padrão para um controle de edição. O comportamento padrão oculta a seleção quando o controle perde o foco de entrada e inverte a seleção quando o controle recebe o foco de entrada. Se você especificar [**es \_ NOHIDESEL**](edit-control-styles.md), o texto selecionado será invertido, mesmo que o controle não tenha o foco.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**\_número es**</dt> </dl>                | Permite que apenas os dígitos sejam inseridos no controle de edição.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**\_senha es**</dt> </dl>          | Exibe um asterisco ( \* ) para cada caractere digitado no controle de edição. Esse estilo é válido somente para controles de edição de linha única.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ somente leitura**</dt> </dl>          | Impede que o usuário digite ou edite texto no controle de edição.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ à direita**</dt> </dl>                   | Alinha o texto à direita em um controle de linha única ou de edição de várias linhas.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**ES \_ WANTRETURN**</dt> </dl>    | Especifica que um retorno de carro será inserido quando o usuário pressionar a tecla ENTER ao inserir texto em um controle de edição de várias linhas em uma caixa de diálogo. Se você não especificar esse estilo, pressionar a tecla ENTER terá o mesmo efeito que pressionar o botão de ação padrão da caixa de diálogo. Esse estilo não tem efeito sobre um controle de edição de linha única.<br/>                   |



Os controles de edição avançados não dão suporte aos seguintes estilos de controle de edição.

-   [**s \_ minúsculas**](edit-control-styles.md)
-   [**ES \_ OEMCONVERT**](edit-control-styles.md)
-   [**ES \_ maiúsculas**](edit-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WinUser. h</dt> </dl> |



 

