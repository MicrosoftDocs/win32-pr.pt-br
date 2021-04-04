---
title: Mensagem de EM_SETSTORYTYPE (RichEdit. h)
description: Define o tipo de história.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Controles de EM_SETSTORYTYPE de mensagens do Windows
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
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824303"
---
# <a name="em_setstorytype-message"></a>\_Mensagem em SEThistóriatype

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

O novo tipo de história. Para obter uma lista de tipos de história, consulte em [**\_ gethistóriatype**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O tipo de história que foi definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





