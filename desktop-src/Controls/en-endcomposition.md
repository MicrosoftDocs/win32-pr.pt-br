---
title: EN_ENDCOMPOSITION código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário inseriu novos dados ou terminou de inserir dados ao usar o IME ou a estrutura de serviços de texto.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454704"
---
# <a name="en_endcomposition-notification-code"></a>\_Código de notificação de ENDcomposição

Notifica uma janela pai do controle de edição rico que o usuário inseriu novos dados ou terminou de inserir dados ao usar o IME ou a [estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework).


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) que recebe informações sobre a condição de composição final.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

