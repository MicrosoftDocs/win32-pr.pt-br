---
title: Mensagem de STM_SETICON (WinUser. h)
description: Um aplicativo envia a \_ mensagem de AUTOÍCONE STM para associar um ícone a um controle de ícone.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- controles de Windows de mensagem de STM_SETICON
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff1cbaa6a1083751b3619392fbb0d3b60695e829907c2dfe27fdb41170e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281416"
---
# <a name="stm_seticon-message"></a>\_Mensagem de SETICON STM

Um aplicativo envia a mensagem de **\_ autoícone STM** para associar um ícone a um controle de ícone.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o ícone a ser associado ao controle de ícone.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um identificador para o ícone associado anteriormente ao controle de ícone ou zero se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**STM \_ GETicon**](stm-geticon.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

