---
title: Mensagem de ICM_SETSTATE (VFW. h)
description: A \_ mensagem ICM SetState notifica um driver de compactação de vídeo para definir o estado do compressor. Você pode enviar essa mensagem explicitamente ou usando a macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- Multimídia do Windows de mensagem ICM_SETSTATE
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
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779617"
---
# <a name="icm_setstate-message"></a>\_Mensagem SETstate do ICM

A mensagem **ICM \_ SetState** notifica um driver de compactação de vídeo para definir o estado do compressor. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .


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

As informações usadas por essa mensagem são privadas e específicas para um determinado compressor. Os aplicativos cliente devem usar essa mensagem somente para restaurar as informações obtidas anteriormente com a mensagem [**ICM \_ GetState**](icm-getstate.md) e devem usar a mensagem [**ICM \_ Configure**](icm-configure.md) para ajustar a configuração de um driver de compactação de vídeo.

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

 

 





