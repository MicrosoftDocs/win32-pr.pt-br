---
title: Mensagem de PBM_SETMARQUEE (commctrl. h)
description: Define a barra de progresso para o modo de letreiro. Isso faz com que a barra de progresso se mova como um letreiro.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- controles de Windows de mensagem de PBM_SETMARQUEE
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
# <a name="pbm_setmarquee-message"></a>\_Mensagem SETmarquee do PBM

Define a barra de progresso para o modo de letreiro. Isso faz com que a barra de progresso se mova como um letreiro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se o modo de letreiro deve ser ativado ou desativado.

</dd> <dt>

*lParam* 
</dt> <dd>Tempo, em milissegundos, entre as atualizações de animação do letreiro digital. Se esse parâmetro for zero, a animação do letreiro digital será atualizada a cada 30 milissegundos.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Use esta mensagem quando você não souber a quantidade de progresso para a conclusão, mas quiser indicar que o progresso está sendo feito.

Envie a **mensagem \_ setmarquee do PBM** para iniciar ou parar a animação.

> [!Note]  
> Você deve definir o estilo de controle [**como \_ marca de marcação PBS**](progress-bar-control-styles.md) antes de tentar iniciar a animação.

 

> [!Note]  
> Esta mensagem requer ComCtl32.dll versão 6, 0 ou posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





