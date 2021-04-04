---
title: Mensagem de STM_SETICON (WinUser. h)
description: Um aplicativo envia a \_ mensagem de AUTOÍCONE STM para associar um ícone a um controle de ícone.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Controles de STM_SETICON de mensagens do Windows
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
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008920"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é um identificador para o ícone associado anteriormente ao controle de ícone ou zero se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



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

 

