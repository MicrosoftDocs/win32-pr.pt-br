---
title: SB_SETPARTS mensagem (Commctrl.h)
description: Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS controles Windows mensagem
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
ms.openlocfilehash: a63694ba40eb77cd887454b634ba8cdd2bff2c6ee7bb75beb9a7230eb3d1e1d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637026"
---
# <a name="sb_setparts-message"></a>Mensagem SB \_ SETPARTS

Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de partes a serem definidas (não pode ser maior que 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de inteiros. O número de elementos é especificado em *wParam*. Cada elemento especifica a posição, nas coordenadas do cliente, da borda direita da parte correspondente. Se um elemento for -1, a borda direita da parte correspondente se estenderá até a borda da janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





