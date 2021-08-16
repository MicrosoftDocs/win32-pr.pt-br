---
title: CCM_DPISCALE mensagem (Commctrl.h)
description: Habilita o dimensionamento automático de dpi (pontos altos por polegada) em controles Tree-View, controles List-View, controles ComboBoxEx, controles de header, botões, controles de barra de ferramentas, controles de animação e listas de imagens.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE controles de Windows mensagem
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e72cb8ac3acf413e4381580a4ecf38a4f5bd4b2f5b03d6cff7d7abb85c1f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320246"
---
# <a name="ccm_dpiscale-message"></a>Mensagem \_ DPISCALE do CCM

Habilita o dimensionamento automático de dpi (pontos altos por polegada) em controles de Modo de Exibição de [Árvore,](tree-view-controls.md)controles [list-View](list-view-control-reference.md), controles [ComboBoxEx,](comboboxex-controls.md) [controles](buttons.md)de [header](header-controls.md), [botões,](toolbar-controls-overview.md)controles de barra de [ferramentas,](animation-control-overview.md)controles de animação e Listas de [imagens](image-lists.md).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Definido como **TRUE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Início Rápido e [Barra de Tarefas](/windows/desktop/shell/taskbar) não devem especificar um dimensionamento dpi, pois as imagens já estão dimensionados.

Qualquer controle que use uma lista de imagens criada com a métrica SmallIcon não deve dimensionar seus ícones.

> [!Note]  
> Para usar essa API, você deve fornecer um manifesto que especifique Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

