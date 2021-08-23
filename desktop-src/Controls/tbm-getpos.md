---
title: Mensagem de TBM_GETPOS (commctrl. h)
description: Recupera a posição lógica atual do controle deslizante em um TrackBar. As posições lógicas são os valores inteiros no intervalo de TrackBar de mínimo para as posições do controle deslizante máximo.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- controles de Windows de mensagem de TBM_GETPOS
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ed3b8afed7b96e657984a437ff54b1099f196b8dc3d0035468835152b5a841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078080"
---
# <a name="tbm_getpos-message"></a>\_Mensagem tbm GETPOS

Recupera a posição lógica atual do controle deslizante em um TrackBar. As posições lógicas são os valores inteiros no intervalo de TrackBar de mínimo para as posições do controle deslizante máximo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que especifica a posição lógica atual do controle deslizante do TrackBar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TBM \_ SETPOS**](tbm-setpos.md)
</dt> </dl>

 

 





