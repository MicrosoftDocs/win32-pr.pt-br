---
title: Mensagem de MCIWNDM_VALIDATEMEDIA (VFW. h)
description: A \_ mensagem MCIWNDM VALIDATEMEDIA atualiza os locais inicial e final do conteúdo, a posição atual no conteúdo e o TrackBar de acordo com o formato de hora atual.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- Multimídia do Windows de mensagem MCIWNDM_VALIDATEMEDIA
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499252"
---
# <a name="mciwndm_validatemedia-message"></a>\_Mensagem MCIWNDM VALIDATEMEDIA

A mensagem **MCIWNDM \_ VALIDATEMEDIA** atualiza os locais inicial e final do conteúdo, a posição atual no conteúdo e o TrackBar de acordo com o formato de hora atual. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Normalmente, você não precisa usar essa macro; no entanto, se seu aplicativo alterar o formato de hora de um dispositivo sem usar MCIWnd; os locais inicial e final do conteúdo, bem como o TrackBar, continuam a usar o formato antigo. Você pode usar essa macro para atualizar esses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





