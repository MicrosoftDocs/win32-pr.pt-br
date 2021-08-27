---
title: EM_SETSTORYTYPE mensagem (Richedit.h)
description: Define o tipo de história.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e09c62c50441857aac6f4018800de7a145081d64de49cdf7e9ca673a5370db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062876"
---
# <a name="em_setstorytype-message"></a>Mensagem EM \_ SETSTORYTYPE

Define o tipo de história.


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da história.

</dd> <dt>

*lParam* 
</dt> <dd>

O novo tipo de história. Para ver uma lista de tipos de história, [**consulte EM \_ GETSTORYTYPE**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O tipo de história que foi definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





