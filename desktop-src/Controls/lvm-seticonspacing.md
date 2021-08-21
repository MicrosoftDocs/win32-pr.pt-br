---
title: LVM_SETICONSPACING mensagem (Commctrl.h)
description: Define o espaçamento entre ícones em controles de exibição de lista que têm o estilo ícone \_ LVS. Você pode enviar essa mensagem explicitamente ou usando a macro \_ ListView SetIconSpacing.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5897b0ca6aec7763cc24a0ea538f336e7a2f737f2ddc0e7cb52a2145e570db47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019165"
---
# <a name="lvm_seticonspacing-message"></a>Mensagem LVM \_ SETICONSPACING

Define o espaçamento entre ícones em controles de exibição de lista que têm o estilo [**ícone LVS. \_**](list-view-window-styles.md) Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ ListView SetIconSpacing.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a distância, em pixels, a ser definida entre ícones no eixo x. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a distância, em pixels, a ser definida entre ícones no eixo y. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor DWORD** que contém a distância anterior do eixo x na palavra baixa e a distância anterior do eixo y na palavra alta.

## <a name="remarks"></a>Comentários

Os valores *de lParam* são relativos ao canto superior esquerdo de um bitmap de ícone. Portanto, para definir o espaçamento entre ícones que não se sobrepõem, os valores *lParam* devem incluir o tamanho do ícone, além da quantidade de espaço vazio desejada entre os ícones. Valores que não incluem a largura do ícone resultarão em sobreposições.

Ao definir o espaçamento do ícone, os *valores lParam* devem ser definidos como 4 ou maiores. Valores menores não produzirão o layout desejado. Para redefinir os ícones para o espaçamento padrão, defina os *valores lParam* como -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

