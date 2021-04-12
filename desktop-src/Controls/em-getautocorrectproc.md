---
title: Mensagem de EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Obtém um ponteiro para a função AutoCorrectProc definida pelo aplicativo.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Controles de EM_GETAUTOCORRECTPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455279"
---
# <a name="em_getautocorrectproc-message"></a>\_Mensagem em GETAUTOCORRECTPROC

Obtém um ponteiro para a função [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida pelo aplicativo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a função [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**em \_ CALLAUTOCORRECTPROC**](em-callautocorrectproc.md)
</dt> <dt>

[**em \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





