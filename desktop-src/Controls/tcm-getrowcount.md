---
title: Mensagem de TCM_GETROWCOUNT (commctrl. h)
description: Recupera o número atual de linhas de guias em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetRowCount TabCtrl.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- controles de Windows de mensagem de TCM_GETROWCOUNT
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
ms.openlocfilehash: 9e67b2ac40834075b31ccf2415a52c96448b8143dde3d6bc67f9c515e1f601a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104866"
---
# <a name="tcm_getrowcount-message"></a>Mensagem do TCM \_ GETrowcount

Recupera o número atual de linhas de guias em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetRowCount TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de linhas de guias.

## <a name="remarks"></a>Comentários

Somente controles de guia que têm o estilo de [**\_ multilinha de TCS**](tab-control-styles.md) podem ter várias linhas de guias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





