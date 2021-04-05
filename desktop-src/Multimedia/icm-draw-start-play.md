---
title: Mensagem de ICM_DRAW_START_PLAY (VFW. h)
description: A \_ mensagem de \_ início de inicialização ICM \_ fornece as horas de início e de término de uma operação de reprodução para um driver de renderização. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_START_PLAY
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085448"
---
# <a name="icm_draw_start_play-message"></a>\_Iniciar a \_ mensagem de início de \_ execução do ICM

A mensagem de **\_ início de \_ inicialização \_ ICM** fornece as horas de início e de término de uma operação de reprodução para um driver de renderização. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*
</dt> <dd>

Hora de início.

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*
</dt> <dd>

Hora de término.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem precede todos os dados de quadro enviados ao driver de renderização.

As unidades para *lFrom* e *lTo* são especificadas com a mensagem de [**\_ \_ início de empate de ICM**](icm-draw-begin.md) . Para dados de vídeo, normalmente é um número de quadro. Para obter mais informações sobre a taxa de reprodução, consulte os membros **dwRate** e **DwScale** da estrutura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .

Se a hora de término for menor que a hora de início, a direção da reprodução será invertida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





