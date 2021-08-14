---
title: DM_POINTERHITTEST mensagem
description: Enviado para uma janela, quando a entrada do ponteiro é detectada pela primeira vez, para determinar o destino de entrada mais provável para a manipulação direta.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- Mensagens de entrada e notificações de DM_POINTERHITTEST mensagem
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9fda57a0c7084ae0c6ab85514244ed531a182108ec5dce7aae7794de2c38c903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482467"
---
# <a name="dm_pointerhittest-message"></a>DM_POINTERHITTEST mensagem

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Enviado para uma janela, quando a entrada do ponteiro é detectada pela primeira vez, para determinar o destino de entrada mais provável para a [manipulação direta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).

> \[! Fundamental\]  
> Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

NULO

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

