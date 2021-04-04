---
title: Mensagem de STM_GETICON (WinUser. h)
description: Um aplicativo envia a \_ mensagem de GETICON STM para recuperar um identificador para o ícone associado a um controle estático que tem o \_ estilo de ícone SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Controles de STM_GETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085286"
---
# <a name="stm_geticon-message"></a>\_Mensagem de GETICON STM

Um aplicativo envia a mensagem de **\_ GetIcon STM** para recuperar um identificador para o ícone associado a um controle estático que tem o \_ estilo de ícone SS.

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

O valor de retorno é um identificador para o ícone, ou **NULL** se o controle estático não tiver nenhum ícone associado ou se ocorreu um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ícone STM**](stm-seticon.md)
</dt> </dl>

 

 





