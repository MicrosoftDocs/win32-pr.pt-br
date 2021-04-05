---
title: Mensagem de TBM_GETBUDDY (commctrl. h)
description: Recupera o identificador para uma janela de amigo do controle TrackBar em um determinado local. O local especificado é relativo à orientação do controle (horizontal ou vertical).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Controles de TBM_GETBUDDY de mensagens do Windows
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
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919226"
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

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a janela Buddy no local especificado por *wParam* ou **NULL** se não existir nenhuma janela Buddy nesse local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





