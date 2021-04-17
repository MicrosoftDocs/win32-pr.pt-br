---
title: Sinalizadores de máscara de evento de controle de edição avançada (RichEdit. h)
description: A máscara de evento especifica quais códigos de notificação um controle de edição avançado envia para sua janela pai. A máscara de evento pode ser None ou uma combinação desses valores.
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006a6d82e7aa4958b03360d05d29a78564f99db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754805"
---
# <a name="rich-edit-control-event-mask-flags"></a>Sinalizadores de máscara de evento de controle de edição avançada

A máscara de evento especifica quais códigos de notificação um controle de edição avançado envia para sua janela pai. A máscara de evento pode ser None ou uma combinação desses valores.



| Constante                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**ENM \_ alterar**</dt> </dl>                                  | Envia notificações de [ \_ alteração](en-change--rich-edit-control-.md) .<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**ENM \_ CLIPFORMAT**</dt> </dl>                      | Envia notificações [en \_ CLIPFORMAT](/windows/desktop/Controls/en-clipformat) .<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**ENM \_ CORRECTTEXT**</dt> </dl>                   | Envia notificações [en \_ CORRECTTEXT](en-correcttext.md) .<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**ENM \_ DRAGDROPDONE**</dt> </dl>                | Envia notificações [en \_ DRAGDROPDONE](en-dragdropdone.md) .<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**ENM \_ DropFiles**</dt> </dl>                         | Envia notificações [en \_ DropFiles](en-dropfiles.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**ENM \_ IMECHANGE**</dt> </dl>                         | Somente o Microsoft Rich Edit 1,0: envia notificações [en \_ IMECHANGE](en-imechange.md) quando o status de conversão do IME foi alterado. Somente para versões em idiomas asiáticos do sistema operacional.<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**ENM \_**</dt> </dl>                         | Envia notificações [en \_ MSGFILTER](en-msgfilter.md) para eventos de teclado.<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**LINK do ENM \_**</dt> </dl>                                        | **Edição avançada 2,0 e posterior:** Envia notificações de [ \_ link](en-link.md) quando o ponteiro do mouse está sobre o texto que tem o \_ link CFE e uma das várias ações do mouse é executada.<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**ENM \_ LOWFIRTF**</dt> </dl>                            | Envia notificações [en \_ LOWFIRTF](en-lowfirtf.md) .<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**ENM \_ MOUSEEVENTS**</dt> </dl>                   | Envia notificações [en \_ MSGFILTER](en-msgfilter.md) para eventos de mouse.<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**ENM \_ OBJECTposições**</dt> </dl>       | Envia notificações de [ \_ objectposições en](en-objectpositions.md) .<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**ENM \_ PARAGRAPHEXPANDED**</dt> </dl> | Envia notificações [en \_ PARAGRAPHEXPANDED](/windows/desktop/Controls/en-paragraphexpanded) .<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**ENM \_ protegido**</dt> </dl>                         | Envia notificações do [en \_ Protected](en-protected.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**ENM \_ REQUESTRESIZE**</dt> </dl>             | Envia notificações [en \_ REQUESTRESIZE](en-requestresize.md) .<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**ENM \_ Scroll**</dt> </dl>                                  | Envia notificações [en \_ HSCROLL](en-hscroll.md) e [en \_ VSCROLL](en-vscroll.md) .<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**ENM \_ SCROLLEVENTS**</dt> </dl>                | Envia notificações [en \_ MSGFILTER](en-msgfilter.md) para eventos de roda do mouse.<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**ENM \_ SELCHANGE**</dt> </dl>                         | Envia notificações [en \_ SELCHANGE](en-selchange.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**atualização do ENM \_**</dt> </dl>                                  | Envia notificações de [ \_ atualização de en](en-update.md) . <br/> **Edição avançada 2,0 e posteriores:** esse sinalizador é ignorado e as notificações de [ \_ atualização do en](en-update.md) são sempre enviadas. No entanto, se o Rich Edit 3,0 emula o Microsoft Rich Edit 1,0, você deve usar esse sinalizador para enviar \_ notificações de atualização.<br/> |



## <a name="remarks"></a>Comentários

A máscara de evento padrão é ENM \_ nenhuma, caso em que nenhuma notificação é enviada para a janela pai. Você pode recuperar e definir a máscara de evento para um controle de edição rico usando as mensagens em [**\_ GETEVENTMASK**](em-geteventmask.md) e em [**\_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>RichEdit. h</dt> </dl> |



 

