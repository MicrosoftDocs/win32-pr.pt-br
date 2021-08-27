---
title: Mensagem de CB_SETCUEBANNER (WinUser. h)
description: Define o texto da faixa de indicação que é exibido para o controle de edição de uma caixa de combinação.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- controles de Windows de mensagem de CB_SETCUEBANNER
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
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089036"
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

## <a name="return-value"></a>Valor retornado

Retornará 1 se for bem-sucedido ou um valor de erro de outra forma.

## <a name="remarks"></a>Comentários

A faixa de indicação é o texto exibido no controle de edição de uma caixa de combinação quando não há seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Recursos da caixa de combinação](combo-box-features.md)
</dt> </dl>

 

 





