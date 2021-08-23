---
title: HDN_DROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho para seu pai quando a seta suspensa no controle de cabeçalho é clicada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN código de notificação Windows controles
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a7e423c40fa655a9eca0e5b97c20a2d61add1e6c0b7f66b65a69afdc32a55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435566"
---
# <a name="hdn_dropdown-notification-code"></a>\_Código de notificação da lista suspensa HDN

Enviado por um controle de cabeçalho para seu pai quando a seta suspensa no controle de cabeçalho é clicada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O exemplo na seção sintaxe mostra como o receptor de notificação converte **lParam** para recuperar a estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contém a ID do controle que envia essa mensagem.

Essa mensagem será enviada somente se o estilo HDF \_ SPLITBUTTON estiver definido no item de cabeçalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





