---
title: Estilos de controle rebar (CommCtrl. h)
description: Os controles Rebar dão suporte a uma variedade de estilos de controle, além dos estilos de janela padrão.
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
ms.openlocfilehash: 67b9f447df2cbf1bb2b956a7ec300d1f29280eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753958"
---
# <a name="rebar-control-styles"></a>Estilos de controle rebar

Os controles Rebar dão suporte a uma variedade de estilos de controle, além dos estilos de janela padrão.



| Constante                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**AUTOSIZE do RBS \_**</dt> </dl>                      | [Versão 4,71](common-control-versions.md). O controle rebar irá alterar automaticamente o layout das faixas quando o tamanho ou a posição do controle for alterado. Uma notificação de [ \_ dimensionamento automático de RBN](rbn-autosize.md) será enviada quando isso ocorrer.<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**\_BANDBORDERS RBS**</dt> </dl>             | [Versão 4,71](common-control-versions.md). O controle rebar exibe linhas estreitas para separar as faixas adjacentes.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**\_DBLCLKTOGGLE RBS**</dt> </dl>          | [Versão 4,71](common-control-versions.md). A faixa Rebar alternará seu estado maximizado ou minimizado quando o usuário clicar duas vezes na banda. Sem esse estilo, o estado maximizado ou minimizado é alternado quando o usuário clica em uma banda.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**\_FIXEDORDER RBS**</dt> </dl>                | [Versão 4,70](common-control-versions.md). O controle rebar sempre exibe as faixas na mesma ordem. Você pode mover as bandas para linhas diferentes, mas a ordem de banda é estática.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**\_REGISTERDROP RBS**</dt> </dl>          | [Versão 4,71](common-control-versions.md). O controle rebar gera códigos de notificação [ \_ GetObject RBN](rbn-getobject.md) quando um objeto é arrastado sobre uma banda no controle. Para receber as \_ notificações GetObject do RBN, inicialize o OLE com uma chamada para [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**Dicas de ferramenta do RBS \_**</dt> </dl>                      | [Versão 4,71](common-control-versions.md). Ainda não tem suporte.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**\_VARHEIGHT RBS**</dt> </dl>                   | [Versão 4,71](common-control-versions.md). O controle rebar exibe as faixas na altura mínima exigida, quando possível. Sem esse estilo, o controle rebar exibe todas as faixas na mesma altura, usando a altura da banda visível mais alta para determinar a altura de outras bandas.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**\_VERTICALGRIPPER RBS**</dt> </dl> | [Versão 4,71](common-control-versions.md). A alça de tamanho será exibida verticalmente em vez de horizontalmente em um controle rebar vertical. Esse estilo é ignorado para controles Rebar que não têm o estilo [**ccs \_ Vert**](common-control-styles.md) .<br/>                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

