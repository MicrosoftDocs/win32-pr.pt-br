---
title: Mensagem de PGM_SETBORDER (commctrl. h)
description: Define o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBorder do pager.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- controles de Windows de mensagem de PGM_SETBORDER
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c44433189c9d791aba1d50372176309682c1361c5b0efe31b11aaa99e9b322b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540526"
---
# <a name="pgm_setborder-message"></a>\_Mensagem de SETborder do PGM

Define o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Novo tamanho da borda, em pixels. Esse valor não deve ser maior que o botão de pager ou menor que zero. Se *lParam* for muito grande, a borda será desenhada com o mesmo tamanho do botão. Se *lParam* for negativo, o tamanho da borda será definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor INT que contém o tamanho da borda anterior, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





