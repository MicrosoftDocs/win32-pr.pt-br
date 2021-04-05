---
title: Mensagem de TCM_DESELECTALL (commctrl. h)
description: Redefine os itens em um controle guia, limpando os que foram definidos para o \_ estado TCIS ButtonPressed. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Controles de TCM_DESELECTALL de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086245"
---
# <a name="tcm_deselectall-message"></a>\_Mensagem DESELECTALL de TCM

Redefine os itens em um controle guia, limpando os que foram definidos para o estado [**TCIS \_ ButtonPressed**](tab-control-item-states.md) . Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador que especifica o escopo da desmarcação do item. Se esse parâmetro for definido como **false**, todos os itens da guia serão redefinidos. Se estiver definido como **true**, todos os itens da guia, exceto o selecionado no momento, serão redefinidos.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

Essa mensagem só será significativa se o sinalizador de estilo de [**\_ botões de TCS**](tab-control-styles.md) tiver sido definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





