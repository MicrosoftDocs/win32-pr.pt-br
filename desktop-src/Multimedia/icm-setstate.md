---
title: Mensagem de ICM_SETSTATE (VFW. h)
description: o ICM \_ mensagem setstate notifica um driver de compactação de vídeo para definir o estado do compressor. Você pode enviar essa mensagem explicitamente ou usando a macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- mensagem de ICM_SETSTATE Windows multimídia
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea6cd7aa0314520a30e293a8f029920c22b8baa58e995eed7ff9e5a96dd1b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525806"
---
# <a name="icm_setstate-message"></a>ICM \_ Mensagem SetState

o **ICM mensagem \_ setstate** notifica um driver de compactação de vídeo para definir o estado do compressor. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Ponteiro para um bloco de memória que contém dados de configuração. Você pode especificar **NULL** para esse parâmetro para redefinir o compressor para seu estado padrão.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Tamanho, em bytes, do bloco de memória.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o número de bytes usados pelo compactador, se for bem-sucedido ou zero.

## <a name="remarks"></a>Comentários

As informações usadas por essa mensagem são privadas e específicas para um determinado compressor. os aplicativos cliente devem usar essa mensagem somente para restaurar as informações obtidas anteriormente com a [**ICM mensagem \_ getstate**](icm-getstate.md) e devem usar a mensagem [**ICM \_ configurar**](icm-configure.md) para ajustar a configuração de um driver de compactação de vídeo.

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

 

 





