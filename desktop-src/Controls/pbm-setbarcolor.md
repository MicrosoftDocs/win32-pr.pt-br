---
title: Mensagem de PBM_SETBARCOLOR (commctrl. h)
description: Define a cor da barra de indicadores de progresso no controle da barra de progresso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Controles de PBM_SETBARCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499544"
---
# <a name="pbm_setbarcolor-message"></a>Mensagem do SETBARCOLOR do PBM \_

Define a cor da barra de indicadores de progresso no controle da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O valor **COLORREF** que especifica a nova cor da barra de indicador de progresso. A especificação do \_ valor padrão CLR faz com que a barra de progresso Use sua cor de barra de indicador de andamento padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor da barra de indicadores de progresso anterior ou o \_ padrão CLR se a cor da barra de indicador de progresso for a cor padrão.

## <a name="remarks"></a>Comentários

Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





