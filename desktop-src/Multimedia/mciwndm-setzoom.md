---
title: Mensagem de MCIWNDM_SETZOOM (VFW. h)
description: A \_ mensagem setZoom do MCIWNDM redimensiona uma imagem de vídeo de acordo com um fator de zoom. Essa Marco ajusta o tamanho de uma janela MCIWnd enquanto mantém uma taxa de proporção constante. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETZOOM
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
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454746"
---
# <a name="mciwndm_setzoom-message"></a>Mensagem de MCIWNDM \_ SETzoom

A **mensagem \_ setZoom do MCIWNDM** redimensiona uma imagem de vídeo de acordo com um fator de zoom. Essa Marco ajusta o tamanho de uma janela MCIWnd enquanto mantém uma taxa de proporção constante. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

Fator de zoom expresso como um percentual da imagem original. Especifique 100 para exibir a imagem com seu tamanho criado, 200 para exibir a imagem com duas vezes seu tamanho normal ou 50 para exibir a imagem com metade do tamanho normal.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





