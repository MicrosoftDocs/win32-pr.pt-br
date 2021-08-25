---
title: Mensagem de MCM_SIZERECTTOMIN (commctrl. h)
description: Calcula quantos calendários serão ajustados no retângulo fornecido e, em seguida, retorna o tamanho mínimo que um retângulo precisa para ajustar esse número de calendários. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- controles de Windows de mensagem de MCM_SIZERECTTOMIN
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547b8e401f270cbca1ff666ba0f1eb263ab3f9245f8a51e6874a7627597b9bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799226"
---
# <a name="mcm_sizerecttomin-message"></a>\_Mensagem MCM SIZERECTTOMIN

Calcula quantos calendários serão ajustados no retângulo fornecido e, em seguida, retorna o tamanho mínimo que um retângulo precisa para ajustar esse número de calendários. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Na entrada, contém um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que descreve uma região maior ou igual ao tamanho necessário para se ajustar ao número desejado de calendários. Quando essa função retorna, contém a estrutura de **Rect** mínima que se ajusta a esse número de calendários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não utilizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

