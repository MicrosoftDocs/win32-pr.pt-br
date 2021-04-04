---
title: Mensagem de TCM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetImageList.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Controles de TCM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008846"
---
# <a name="tcm_setimagelist-message"></a>Mensagem do TCM \_ SETimagelist

Atribui uma lista de imagens a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a lista de imagens a ser atribuída ao controle guia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens anterior, ou **NULL** se não houver nenhuma lista de imagens anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





