---
title: Mensagem de CB_SETCUEBANNER (WinUser. h)
description: Define o texto da faixa de indicação que é exibido para o controle de edição de uma caixa de combinação.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Controles de CB_SETCUEBANNER de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009354"
---
# <a name="cb_setcuebanner-message"></a>\_Mensagem de SETCUEBANNER CB

Define o texto da faixa de indicação que é exibido para o controle de edição de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um buffer de cadeia de caracteres Unicode terminada em nulo que contém o texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará 1 se for bem-sucedido ou um valor de erro de outra forma.

## <a name="remarks"></a>Comentários

A faixa de indicação é o texto exibido no controle de edição de uma caixa de combinação quando não há seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Recursos da caixa de combinação](combo-box-features.md)
</dt> </dl>

 

 





