---
title: Mensagem de PBM_SETMARQUEE (commctrl. h)
description: Define a barra de progresso para o modo de letreiro. Isso faz com que a barra de progresso se mova como um letreiro.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Controles de PBM_SETMARQUEE de mensagens do Windows
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
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918792"
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

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





