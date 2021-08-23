---
title: Mensagem de TBM_SETBUDDY (commctrl. h)
description: Atribui uma janela como a janela Buddy para um controle TrackBar. As janelas TrackBar Buddy são exibidas automaticamente em um local em relação à orientação do controle (horizontal ou vertical).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- controles de Windows de mensagem de TBM_SETBUDDY
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f2586c84740cb2d5e8b1f1aadfb910cd241270d3e18363accf1f166c3c35ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167182"
---
# <a name="tbm_setbuddy-message"></a>Mensagem do TBM \_ SETbuddy

Atribui uma janela como a janela Buddy para um controle TrackBar. As janelas TrackBar Buddy são exibidas automaticamente em um local em relação à orientação do controle (horizontal ou vertical).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica o local no qual exibir a janela do Buddy. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**TRUE**</dt> </dl>    | O colega será exibido à esquerda do TrackBar se o controle TrackBar usar o estilo [**TBS \_ na horizontal**](trackbar-control-styles.md) . Se o TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , o colega aparecerá acima do controle TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FOR**</dt> </dl> | O colega será exibido à direita de TrackBar se o controle TrackBar usar o estilo [**TBS \_ na horizontal**](trackbar-control-styles.md) . Se o TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , o colega aparecerá abaixo do controle TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Manipule para a janela que será definida como o colega do controle TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para a janela que foi atribuída anteriormente ao controle nesse local.

## <a name="remarks"></a>Comentários

> [!Note]  
> Os controles TrackBar dão suporte a até duas janelas de amigo. Isso pode ser útil quando você precisa exibir texto ou imagens em cada extremidade do controle.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





