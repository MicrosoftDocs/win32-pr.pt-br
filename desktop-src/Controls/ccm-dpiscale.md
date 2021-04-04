---
title: Mensagem de CCM_DPISCALE (commctrl. h)
description: Habilita o dimensionamento automático de pontos por polegada (DPI) em controles de Tree-View, controles de List-View, controles de ComboBoxEx, controles de cabeçalho, botões, controles de barra de ferramentas, controles de animação e listas de imagens.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Controles de CCM_DPISCALE de mensagens do Windows
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
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085835"
---
# <a name="ccm_dpiscale-message"></a>CCM \_ DPISCALE mensagem

Habilita o dimensionamento automático de pontos por polegada (DPI) em [controles de exibição de árvore](tree-view-controls.md), controles de exibição de [lista](list-view-control-reference.md), [controles de ComboBoxEx](comboboxex-controls.md), controles de [cabeçalho](header-controls.md), [botões](buttons.md), controles de [barra de ferramentas](toolbar-controls-overview.md), [controles de animação](animation-control-overview.md)e [listas de imagens](image-lists.md).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Defina como **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

O início rápido e a [barra de tarefas](/windows/desktop/shell/taskbar) não devem especificar um dimensionamento de DPI, pois as imagens já estão dimensionadas.

Qualquer controle que usa uma lista de imagens criada com a métrica SmallIcon não deve dimensionar seus ícones.

> [!Note]  
> Para usar essa API, você deve fornecer um manifesto que especifique Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

