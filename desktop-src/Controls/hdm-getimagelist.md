---
title: Mensagem de HDM_GETIMAGELIST (commctrl. h)
description: Obtém o identificador para a lista de imagens que foi definida para um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetImageList ou header \_ GetStateImageList do cabeçalho.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Controles de HDM_GETIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644844"
---
# <a name="hdm_getimagelist-message"></a>\_Mensagem HDM GETimagelist

Obtém o identificador para a lista de imagens que foi definida para um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) ou [**header \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) do cabeçalho.

## <a name="parameters"></a>Parâmetros

<dl> <dt>*wParam*</dt> <dd>Um dos seguintes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normal**</dt> </dl> | Indica que esta é uma lista de imagens normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**\_estado HDSIL**</dt> </dl>    | Indica que esta é uma lista de imagens de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um identificador para a lista de imagens definida para o controle de cabeçalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





