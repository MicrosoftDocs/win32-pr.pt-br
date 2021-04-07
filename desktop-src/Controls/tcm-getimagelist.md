---
title: Mensagem de TCM_GETIMAGELIST (commctrl. h)
description: Recupera a lista de imagens associada a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- Controles de TCM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824713"
---
# <a name="tcm_getimagelist-message"></a>Mensagem do TCM \_ GETimagelist

Recupera a lista de imagens associada a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





