---
title: Mensagem de EM_SETOPTIONS (RichEdit. h)
description: Define as opções para um controle de edição rico.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Controles de EM_SETOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085469"
---
# <a name="em_setoptions-message"></a>\_Mensagem em SEToptionss

Define as opções para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a operação, que pode ser um desses valores.



| Valor                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**conjunto de ECOOP \_**</dt> </dl> | Define as opções para as especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ ou**</dt> </dl>    | Combina as opções especificadas com as opções atuais.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ e**</dt> </dl> | Retém somente as opções atuais que também são especificadas por *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**\_XOR ECOOP**</dt> </dl> | Logicamente exclusivas ou as opções atuais com as especificadas por *lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                 | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**AUTOWORDSELECTION de ECO \_**</dt> </dl> | Seleção automática de palavra ao clicar duas vezes.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**AUTOVSCROLL de ECO \_**</dt> </dl>                   | O mesmo que [**s \_ AUTOVSCROLL**](rich-edit-control-styles.md) estilo.<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**AUTOHSCROLL de ECO \_**</dt> </dl>                   | O mesmo que [**s \_ AUTOHSCROLL**](rich-edit-control-styles.md) estilo.<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**NOHIDESEL de ECO \_**</dt> </dl>                         | O mesmo que [**s \_ NOHIDESEL**](rich-edit-control-styles.md) estilo.<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**\_somente leitura do eco**</dt> </dl>                            | O mesmo que o estilo [**\_ ReadOnly**](rich-edit-control-styles.md) .<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**WANTRETURN de ECO \_**</dt> </dl>                      | O mesmo que [**s \_ WANTRETURN**](rich-edit-control-styles.md) estilo.<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**SELECTIONBAR de ECO \_**</dt> </dl>                | O mesmo que [**s \_ SELECTIONBAR**](rich-edit-control-styles.md) estilo.<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**VERTICAL do ECO \_**</dt> </dl>                            | O mesmo que o estilo [**\_ vertical es**](rich-edit-control-styles.md) . Disponível apenas em versões do idioma asiático.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna as opções atuais do controle de edição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estilos de controle de edição avançados**](rich-edit-control-styles.md)
</dt> </dl>

 

 





