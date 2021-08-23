---
title: HDM_GETIMAGELIST mensagem (Commctrl.h)
description: Obtém o alçamento para a lista de imagens que foi definida para um controle de header existente. Você pode enviar essa mensagem explicitamente ou usar a macro \_ GetImageList ou Header \_ GetStateImageList do header.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST controles Windows mensagem
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8149dd4914ceb1835e9e04442492855e9c25340604ed4e4eeb2619c62b88e69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540906"
---
# <a name="hdm_getimagelist-message"></a>Mensagem \_ GETIMAGELIST do HDM

Obtém o alçamento para a lista de imagens que foi definida para um controle de header existente. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) ou [**Header \_ GetStateImageList do header.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist)

## <a name="parameters"></a>Parâmetros

<dl> <dt>*wParam*</dt> <dd>Um dos seguintes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica que essa é uma lista de imagens normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**ESTADO DO \_ HDSIL**</dt> </dl>    | Indica que esta é uma lista de imagens de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um alça para o conjunto de lista de imagens para o controle de header.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





