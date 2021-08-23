---
title: EM_GETAUTOCORRECTPROC mensagem (Richedit.h)
description: Obtém um ponteiro para a função AutoCorrectProc definida pelo aplicativo.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- EM_GETAUTOCORRECTPROC controles Windows mensagem
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
ms.openlocfilehash: 4dc6b5068c1e72c05d7a1b85ee02e57b788cf417f732fe3c2bab8c66d0dcf383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541086"
---
# <a name="em_getautocorrectproc-message"></a>Mensagem EM \_ GETAUTOCORRECTPROC

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

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para a função [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ CALLAUTOCORRECTPROC**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





