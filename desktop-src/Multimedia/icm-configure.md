---
title: Mensagem de ICM_CONFIGURE (VFW. h)
description: A mensagem de configuração de ICM \_ Notifica um driver de compactação de vídeo para exibir sua caixa de diálogo de configuração ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo de configuração.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- Multimídia do Windows de mensagem ICM_CONFIGURE
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
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770165"
---
# <a name="icm_configure-message"></a>Mensagem de configuração de ICM \_

A mensagem de **\_ configuração de ICM** notifica um driver de compactação de vídeo para exibir sua caixa de diálogo de configuração ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Identificador para a janela pai da caixa de diálogo exibida. Você pode determinar se um driver tem uma caixa de diálogo de configuração especificando 1 nesse parâmetro, como na macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.

## <a name="remarks"></a>Comentários

Essa mensagem é diferente da mensagem [**de \_ configuração de drv**](drv-configure.md) usada para configuração de hardware. A caixa de diálogo dessa mensagem deve permitir que o usuário defina e edite o estado interno referenciado pelas mensagens [**ICM \_ GetState**](icm-getstate.md) e [**ICM \_ SetState**](icm-setstate.md) . Por exemplo, essa caixa de diálogo pode permitir que o usuário altere os parâmetros que afetam o nível de qualidade e outras opções de compactação semelhantes.

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

 

 





