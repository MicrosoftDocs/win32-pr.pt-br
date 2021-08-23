---
title: Mensagem de ICM_COMPRESS (VFW. h)
description: o ICM \_ mensagem de compactação notifica um driver de compactação de vídeo para compactar um quadro de dados em um buffer definido pelo aplicativo.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- mensagem de ICM_COMPRESS Windows multimídia
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678466"
---
# <a name="icm_compress-message"></a>ICM \_ COMPACTar mensagem

o **ICM mensagem de \_ compactação** notifica um driver de compactação de vídeo para compactar um quadro de dados em um buffer definido pelo aplicativo.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*ICC*
</dt> <dd>

Ponteiro para uma estrutura [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) . Os seguintes membros dessa estrutura especificam os parâmetros de compactação: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** e **dwQuality**. O driver também deve usar o membro **biSizeImage** da estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associada ao **lpbiOutput** de **ICCOMPRESS** para retornar o tamanho do quadro compactado.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

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

 

