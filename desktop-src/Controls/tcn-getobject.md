---
title: TCN_GETOBJECT código de notificação (commctrl. h)
description: Enviado por um controle guia quando ele tem o \_ \_ estilo estendido REGISTERDROP de TCS e um objeto é arrastado sobre um item de guia no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750935"
---
# <a name="tcn_getobject-notification-code"></a>Código de notificação do TCN \_ GETobject

Enviado por um controle guia quando ele tem o estilo estendido [**\_ \_ REGISTERDROP de TCS**](tab-control-extended-styles.md) e um objeto é arrastado sobre um item de guia no controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre o item de guia no qual o objeto é arrastado e recebe dados que o aplicativo retorna em resposta a essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo que processa esse código de notificação deve retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





