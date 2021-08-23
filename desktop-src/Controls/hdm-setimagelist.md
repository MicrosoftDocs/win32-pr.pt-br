---
title: HDM_SETIMAGELIST mensagem (Commctrl.h)
description: Atribui uma lista de imagens a um controle de header existente. Você pode enviar essa mensagem explicitamente ou usar a macro \_ Header SetImageList ou \_ Header SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST controles de Windows mensagem
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2034a6880721914961b3bd75907df2e7b4e53360ccb3b10162f238068d85031d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435806"
---
# <a name="hdm_setimagelist-message"></a>Mensagem \_ HDM SETIMAGELIST

Atribui uma lista de imagens a um controle de header existente. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ Header SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) ou [**\_ Header SetStateImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist)

## <a name="parameters"></a>Parâmetros

<dl> <dt>*wParam*</dt> <dd>Um dos seguintes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica que essa é uma lista de imagens normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**ESTADO DO \_ HDSIL**</dt> </dl>    | Indica que esta é uma lista de imagens de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para uma lista de imagens.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens associada anteriormente ao controle . Retorna **NULL após** falha ou se nenhuma lista de imagens foi definida anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





