---
title: Mensagem de ICM_GETDEFAULTQUALITY (VFW. h)
description: A \_ mensagem ICM GETDEFAULTQUALITY consulta um driver de compactação de vídeo para fornecer sua configuração de qualidade padrão. Você pode enviar essa mensagem explicitamente ou usando a macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- Multimídia do Windows de mensagem ICM_GETDEFAULTQUALITY
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454807"
---
# <a name="icm_getdefaultquality-message"></a>\_Mensagem GETDEFAULTQUALITY de ICM

A mensagem **ICM \_ GETDEFAULTQUALITY** consulta um driver de compactação de vídeo para fornecer sua configuração de qualidade padrão. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Endereço para conter o valor de qualidade padrão. Os valores de qualidade variam de 0 a 10.000.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.

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

 

 





