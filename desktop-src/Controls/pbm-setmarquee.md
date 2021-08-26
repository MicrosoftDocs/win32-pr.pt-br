---
title: PBM_SETMARQUEE mensagem (Commctrl.h)
description: Define a barra de progresso para o modo de marca. Isso faz com que a barra de progresso se mova como um letreiro.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE controles de Windows mensagem
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f724f87faa6e989fddb17e8d6fb3b115dd04859ea426addb7d4c0b893aff407a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986136"
---
# <a name="pbm_setmarquee-message"></a>Mensagem PBM \_ SETMARQUEE

Define a barra de progresso para o modo de marca. Isso faz com que a barra de progresso se mova como um letreiro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se o modo de letreiro deve ser desligado ou não.

</dd> <dt>

*lParam* 
</dt> <dd>Tempo, em milissegundos, entre atualizações de animação de letreiro. Se esse parâmetro for zero, a animação de letreiro será atualizada a cada 30 milissegundos.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **TRUE.**

## <a name="remarks"></a>Comentários

Use essa mensagem quando você não sabe a quantidade de progresso até a conclusão, mas deseja indicar que o progresso está sendo feito.

Envie a **mensagem PBM \_ SETMARQUEE** para iniciar ou parar a animação.

> [!Note]  
> Você deve definir o estilo de controle como [**PBS \_ MARQUEE**](progress-bar-control-styles.md) antes de tentar iniciar a animação.

 

> [!Note]  
> Essa mensagem requer ComCtl32.dll versão 6.00 ou posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





