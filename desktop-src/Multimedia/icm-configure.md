---
title: ICM_CONFIGURE mensagem (Vfw.h)
description: A ICM configurar notifica um driver de compactação de vídeo para exibir sua caixa de diálogo de configuração ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo \_ de configuração.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d9176415c22a1b79a8dc08ee84db1c77fbd6665f89f615b38d3c60538d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784996"
---
# <a name="icm_configure-message"></a>\_ICM MENSAGEM CONFIGURE

A **ICM \_ configurar** notifica um driver de compactação de vídeo para exibir sua caixa de diálogo de configuração ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICConfigure.**](/windows/desktop/api/Vfw/nf-vfw-icconfigure)


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Lidar com a janela pai da caixa de diálogo exibida. Você pode determinar se um driver tem uma caixa de diálogo de configuração especificando 1 nesse parâmetro, como na macro [**ICQueryConfigure.**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna ICERR \_ OK se o driver dá suporte a essa mensagem ou ICERR \_ SEM SUPORTE caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem é diferente da mensagem [**DRV \_ CONFIGURE**](drv-configure.md) usada para configuração de hardware. A caixa de diálogo dessa mensagem deve permitir que o usuário desemita e edite o estado interno referenciado pelas mensagens [**\_ ICM GETSTATE**](icm-getstate.md) [**e ICM \_ SETSTATE.**](icm-setstate.md) Por exemplo, essa caixa de diálogo pode permitir que o usuário altere os parâmetros que afetam o nível de qualidade e outras opções de compactação semelhantes.

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

 

 





