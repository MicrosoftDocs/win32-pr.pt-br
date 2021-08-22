---
title: EM_HIDEBALLOONTIP mensagem (Commctrl.h)
description: Oculta qualquer dica de balão associada a um controle de edição.
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- EM_HIDEBALLOONTIP controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a25b9380738b29a938ff59d2d80ac996747b9996ade2f5acb773ec6c7b93a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019484"
---
# <a name="em_hideballoontip-message"></a>Mensagem EM \_ HIDEBALLTIP

Oculta qualquer dica de balão associada a um controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, ela retornará **TRUE.** Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Editar \_ HideBalltip**](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





