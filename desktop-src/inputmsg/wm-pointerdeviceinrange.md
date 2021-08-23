---
title: WM_POINTERDEVICEINRANGE mensagem
description: Enviado para uma janela quando um dispositivo de ponteiro é detectado dentro do intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- WM_POINTERDEVICEINRANGE mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 854640d63225945eb19dd56bd092d5b2eb66c2a3cf30c735f3dc64d7594e7502
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602317"
---
# <a name="wm_pointerdeviceinrange-message"></a>WM_POINTERDEVICEINRANGE mensagem

Enviado para uma janela quando um dispositivo de ponteiro é detectado dentro do intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade.

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Obter informações adicionais específicas de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Obter informações adicionais específicas de mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o aplicativo processa essa mensagem, ele deve retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

