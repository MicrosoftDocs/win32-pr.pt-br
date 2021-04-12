---
title: Mensagem de SB_SETPARTS (commctrl. h)
description: Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Controles de SB_SETPARTS de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499594"
---
# <a name="sb_setparts-message"></a>\_Mensagem de CONpartes da SB

Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de partes a serem definidas (não pode ser maior que 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de inteiros. O número de elementos é especificado em *wParam*. Cada elemento Especifica a posição, nas coordenadas do cliente, da borda direita da parte correspondente. Se um elemento for-1, a borda direita da parte correspondente se estenderá à borda da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





