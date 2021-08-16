---
title: WM_CAP_PAL_OPEN mensagem (Vfw.h)
description: A mensagem WM CAP PAL OPEN carrega uma nova paleta de um \_ \_ arquivo de \_ paleta e a passa para um driver de captura.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29cb831ca0128b0562d6ee53b8e66309d2e1dbd91803dab13202dc4a6723bfa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800575"
---
# <a name="wm_cap_pal_open-message"></a>Mensagem WM \_ CAP \_ PAL \_ OPEN

A **mensagem WM CAP PAL \_ \_ \_ OPEN** carrega uma nova paleta de um arquivo de paleta e a passa para um driver de captura. Arquivos de paleta normalmente usam a extensão de nome de arquivo . Amigo. Um driver de captura usa uma paleta quando exigido pelo formato de imagem digitalizado especificado. Você pode enviar essa mensagem explicitamente ou usando a [**macro capPaletteOpen.**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen)


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome de arquivo da paleta.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) a função de retorno de chamada de erro será chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





