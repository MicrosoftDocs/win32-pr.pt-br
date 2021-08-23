---
title: ICM_GETDEFAULTQUALITY mensagem (Vfw.h)
description: A ICM getDEFAULTQUALITY consulta um driver de \_ compactação de vídeo para fornecer sua configuração de qualidade padrão. Você pode enviar essa mensagem explicitamente ou usando a macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY mensagem Windows Multimídia
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
ms.openlocfilehash: df9c27527cea53c4b4eca6cf75babef3a41f80732d8ecf7a18528c07d6d9311b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525906"
---
# <a name="icm_getdefaultquality-message"></a>\_ICM Mensagem GETDEFAULTQUALITY

A **ICM \_ mensagem GETDEFAULTQUALITY** consulta um driver de compactação de vídeo para fornecer sua configuração de qualidade padrão. Você pode enviar essa mensagem explicitamente ou usando a [**macro ICGetDefaultQuality.**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)


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

Retorna ICERR \_ OK se o driver dá suporte a essa mensagem ou ICERR \_ SEM SUPORTE caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





