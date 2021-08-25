---
title: Mensagem de ICM_GETSTATE (VFW. h)
description: a ICM \_ mensagem getstate consulta um driver de compactação de vídeo para retornar sua configuração atual em um bloco de memória ou para determinar a quantidade de memória necessária para recuperar as informações de configuração.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- mensagem de ICM_GETSTATE Windows multimídia
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bf21d808752b8a3ac3ba71a8593cd6dc577b3af4f34f421682d126c73b3578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784946"
---
# <a name="icm_getstate-message"></a>ICM \_ Mensagem GetState

a **ICM mensagem \_ getstate** consulta um driver de compactação de vídeo para retornar sua configuração atual em um bloco de memória ou para determinar a quantidade de memória necessária para recuperar as informações de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Ponteiro para um bloco de memória para conter as informações de configuração atuais. Você pode especificar **NULL** para esse parâmetro para determinar a quantidade de memória necessária para as informações de configuração, como em [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Tamanho, em bytes, do bloco de memória.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Se *VP* for **NULL**, retornará a quantidade de memória, em bytes, necessária para as informações de configuração.

Se *VP* não for **NULL**, retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A estrutura usada para representar as informações de configuração é específica do driver e é definida pelo driver.

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

 

 





