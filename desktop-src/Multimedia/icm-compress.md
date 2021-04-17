---
title: Mensagem de ICM_COMPRESS (VFW. h)
description: A \_ mensagem de compactação ICM notifica um driver de compactação de vídeo para compactar um quadro de dados em um buffer definido pelo aplicativo.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS
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
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748130"
---
# <a name="icm_compress-message"></a>\_Mensagem de compactação ICM

A mensagem de **\_ compactação ICM** notifica um driver de compactação de vídeo para compactar um quadro de dados em um buffer definido pelo aplicativo.


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

 

