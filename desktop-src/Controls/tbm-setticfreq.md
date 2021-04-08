---
title: Mensagem de TBM_SETTICFREQ (commctrl. h)
description: Define a frequência de intervalo para marcas de escala em um TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Controles de TBM_SETTICFREQ de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009118"
---
# <a name="tbm_setticfreq-message"></a>\_Mensagem tbm SETTICFREQ

Define a frequência de intervalo para marcas de escala em um TrackBar. Por exemplo, se a frequência for definida como dois, uma marca de escala será exibida para todos os outros incrementos no intervalo do TrackBar. A configuração padrão para a frequência é uma; ou seja, cada incremento no intervalo é associado a uma marca de escala.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Frequência das marcas de escala.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O TrackBar deve ter o estilo de [**\_ autotiques TBS**](trackbar-control-styles.md) para usar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





