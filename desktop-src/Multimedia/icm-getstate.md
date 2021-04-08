---
title: Mensagem de ICM_GETSTATE (VFW. h)
description: A \_ mensagem ICM GetState consulta um driver de compactação de vídeo para retornar sua configuração atual em um bloco de memória ou para determinar a quantidade de memória necessária para recuperar as informações de configuração.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- Multimídia do Windows de mensagem ICM_GETSTATE
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
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086512"
---
# <a name="icm_getstate-message"></a>\_Mensagem de GETstate do ICM

A mensagem **ICM \_ GetState** consulta um driver de compactação de vídeo para retornar sua configuração atual em um bloco de memória ou para determinar a quantidade de memória necessária para recuperar as informações de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


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

 

 





