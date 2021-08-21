---
title: Mensagem de TBM_SETTIC (commctrl. h)
description: Define uma marca de escala em um TrackBar na posição lógica especificada.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- controles de Windows de mensagem de TBM_SETTIC
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f286a2f03e318629a10651d066da5aa6cfe70aa293f242ad7508d0ef4739a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540016"
---
# <a name="tbm_settic-message"></a>Mensagem de TBM de Conguração \_

Define uma marca de escala em um TrackBar na posição lógica especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Posição da marca de escala. Esse parâmetro pode ser qualquer um dos valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a marca de escala estiver definida ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Um TrackBar cria suas próprias primeiras e últimas marcas de escala. Não use essa mensagem para definir a primeira e a última marca de escala.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





