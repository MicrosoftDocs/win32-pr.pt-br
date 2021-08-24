---
title: Mensagem de DRV_LOAD (mmsystem. h)
description: Notifica o driver de que ele foi carregado. O driver deve certificar-se de que qualquer hardware e drivers de suporte necessários para funcionar corretamente estão presentes.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- mensagem de DRV_LOAD Windows multimídia
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74b8d0663e96f0dc700739c7b8b5f9304d478ed02bf9493f24d03a506c14a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678706"
---
# <a name="drv_load-message"></a>Mensagem de carregamento de DRV \_

Notifica o driver de que ele foi carregado. O driver deve certificar-se de que qualquer hardware e drivers de suporte necessários para funcionar corretamente estão presentes.

## <a name="parameters"></a>Parâmetros

O parâmetro *hdrvr* é sempre zero. Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.

## <a name="return-value"></a>Valor Retornado

Retornará zero, se for bem-sucedido ou zero.

## <a name="remarks"></a>Comentários

A mensagem de **\_ carregamento de drv** é sempre a primeira mensagem que um driver de dispositivo recebe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





