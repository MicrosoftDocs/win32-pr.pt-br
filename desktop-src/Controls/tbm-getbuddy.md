---
title: Mensagem de TBM_GETBUDDY (commctrl. h)
description: Recupera o identificador para uma janela de amigo do controle TrackBar em um determinado local. O local especificado é relativo à orientação do controle (horizontal ou vertical).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- controles de Windows de mensagem de TBM_GETBUDDY
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e03053981ed16b97d68d5b2f0c77db64062d64fd2df7b5a347e4757736d4844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829610"
---
# <a name="tbm_getbuddy-message"></a>Mensagem do TBM \_ GETbuddy

Recupera o identificador para uma janela de amigo do controle TrackBar em um determinado local. O local especificado é relativo à orientação do controle (horizontal ou vertical).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que indica qual identificador de janela de amigo será recuperado, por local relativo. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                    | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VERDADEIRO * * * *</dt> </dl>    | Recupera o identificador para o amigo à esquerda do TrackBar. Se o controle TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , a mensagem recuperará o colega acima do TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Recupera o identificador para o amigo à direita do TrackBar. Se o controle TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , a mensagem recuperará o colega abaixo do TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para a janela Buddy no local especificado por *wParam* ou **NULL** se não existir nenhuma janela Buddy nesse local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





