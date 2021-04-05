---
title: Mensagem de TCM_GETROWCOUNT (commctrl. h)
description: Recupera o número atual de linhas de guias em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetRowCount TabCtrl.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Controles de TCM_GETROWCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824711"
---
# <a name="tcm_getrowcount-message"></a>Mensagem do TCM \_ GETrowcount

Recupera o número atual de linhas de guias em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetRowCount TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de linhas de guias.

## <a name="remarks"></a>Comentários

Somente controles de guia que têm o estilo de [**\_ multilinha de TCS**](tab-control-styles.md) podem ter várias linhas de guias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





