---
title: Mensagem de TBM_CLEARTICS (commctrl. h)
description: Remove as marcas de escala atuais de um TrackBar. Essa mensagem não remove a primeira e a última marca de escala, que são criadas automaticamente pelo TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Controles de TBM_CLEARTICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454881"
---
# <a name="tbm_cleartics-message"></a>\_Mensagem tbm CLEARTICS

Remove as marcas de escala atuais de um TrackBar. Essa mensagem não remove a primeira e a última marca de escala, que são criadas automaticamente pelo TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, o TrackBar será redesenhado depois que as marcas de escala forem limpas. Se esse parâmetro for **false**, a mensagem limpará as marcas de escala, mas não redesenhará o TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





