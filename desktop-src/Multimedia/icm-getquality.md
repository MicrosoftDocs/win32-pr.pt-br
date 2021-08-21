---
title: ICM_GETQUALITY mensagem (Vfw.h)
description: A ICM GETQUALITY consulta um driver de compactação \_ de vídeo para retornar sua configuração de qualidade atual.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cef214fe36c713e63659fcbd4dde2021c8d410b36ea9f5525ed54c76c5c4b6a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495856"
---
# <a name="icm_getquality-message"></a>\_ICM Mensagem GETQUALITY

A **ICM \_ GETQUALITY** consulta um driver de compactação de vídeo para retornar sua configuração de qualidade atual.


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Endereço para conter o valor de qualidade atual. Os valores de qualidade variam de 0 a 10.000.

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

 

 





