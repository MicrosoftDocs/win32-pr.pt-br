---
title: Rebar estilos de controle (CommCtrl.h)
description: Os controles de barra de rebar suportam uma variedade de estilos de controle, além dos estilos de janela padrão.
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e40a2f93820391d0c2b928c67784157c1f58d7995d42c51df5373d642bd796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078520"
---
# <a name="rebar-control-styles"></a>Rebar estilos de controle

Os controles de barra de rebar suportam uma variedade de estilos de controle, além dos estilos de janela padrão.



| Constante                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**RBS \_ AUTOSIZE**</dt> </dl>                      | [Versão 4.71.](common-control-versions.md) O controle rebar alterará automaticamente o layout das faixas quando o tamanho ou a posição do controle mudar. Uma [notificação \_ RBN AUTOSIZE](rbn-autosize.md) será enviada quando isso ocorrer.<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**RBS \_ BANDBORDERS**</dt> </dl>             | [Versão 4.71.](common-control-versions.md) O controle rebar exibe linhas estreitas para separar as faixas adjacentes.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**RBS \_ DBLCLKTOGGLE**</dt> </dl>          | [Versão 4.71.](common-control-versions.md) A faixa de barra de rebar alterna seu estado maximizada ou minimizada quando o usuário clica duas vezes na banda. Sem esse estilo, o estado maximizada ou minimizado é alternado quando o usuário clica com um único clique na banda.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**RBS \_ FIXEDORDER**</dt> </dl>                | [Versão 4.70.](common-control-versions.md) O controle de barra de rebar sempre exibe faixas na mesma ordem. Você pode mover faixas para linhas diferentes, mas a ordem da banda é estática.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**RBS \_ REGISTERDROP**</dt> </dl>          | [Versão 4.71.](common-control-versions.md) O controle de barra de rebar gera códigos de notificação [ \_ GETOBJECT do RBN](rbn-getobject.md) quando um objeto é arrastado sobre uma faixa no controle . Para receber as notificações GETOBJECT do RBN, inicialize o OLE com uma chamada para \_ [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**DICAS DE FERRAMENTAS do RBS \_**</dt> </dl>                      | [Versão 4.71.](common-control-versions.md) Ainda não há suporte.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**RBS \_ VARHEIGHT**</dt> </dl>                   | [Versão 4.71.](common-control-versions.md) O controle rebar exibe faixas na altura mínima necessária, quando possível. Sem esse estilo, o controle rebar exibe todas as faixas na mesma altura, usando a altura da faixa visível mais alta para determinar a altura de outras faixas.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**RBS \_ VERTICALGRIPPER**</dt> </dl> | [Versão 4.71.](common-control-versions.md) A barra de tamanho será exibida verticalmente em vez de horizontalmente em um controle de barra vertical. Esse estilo é ignorado para controles de barra de rebar que não têm o [**estilo \_ VERT do CCS.**](common-control-styles.md)<br/>                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

