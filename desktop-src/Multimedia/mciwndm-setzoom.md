---
title: MCIWNDM_SETZOOM mensagem (Vfw.h)
description: A mensagem SETZOOM MCIWNDM \_ resize uma imagem de vídeo de acordo com um fator de zoom. Esse marco ajusta o tamanho de uma janela MCIWnd, mantendo uma taxa de proporção constante. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcdd40206332df442bbae32975b0d888bbe39bc377a189d40e215888e4a6d0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807576"
---
# <a name="mciwndm_setzoom-message"></a>Mensagem SETZOOM MCIWNDM \_

A **mensagem \_ SETZOOM MCIWNDM** resize uma imagem de vídeo de acordo com um fator de zoom. Esse marco ajusta o tamanho de uma janela MCIWnd, mantendo uma taxa de proporção constante. Você pode enviar essa mensagem explicitamente ou usando a [**macro MCIWndSetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

Fator de zoom expresso como uma porcentagem da imagem original. Especifique 100 para exibir a imagem em seu tamanho autoral, 200 para exibir a imagem em duas vezes seu tamanho normal ou 50 para exibir a imagem pela metade do tamanho normal.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





