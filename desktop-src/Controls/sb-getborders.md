---
title: Mensagem de SB_GETBORDERS (commctrl. h)
description: Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Controles de SB_GETBORDERS de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086023"
---
# <a name="sb_getborders-message"></a>Mensagem da SB \_ GETborders

Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de inteiros que tem três elementos. O primeiro elemento recebe a largura da borda horizontal, a segunda recebe a largura da borda vertical e a terceira recebe a largura da borda entre retângulos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

As bordas determinam o espaçamento entre a borda externa da janela e os retângulos dentro da janela que contêm texto. As bordas também determinam o espaçamento entre retângulos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





