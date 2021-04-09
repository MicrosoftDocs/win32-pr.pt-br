---
title: Mensagem de TBM_SETTIC (commctrl. h)
description: Define uma marca de escala em um TrackBar na posição lógica especificada.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Controles de TBM_SETTIC de mensagens do Windows
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
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085334"
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

## <a name="return-value"></a>Retornar valor

Retornará **true** se a marca de escala estiver definida ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Um TrackBar cria suas próprias primeiras e últimas marcas de escala. Não use essa mensagem para definir a primeira e a última marca de escala.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





