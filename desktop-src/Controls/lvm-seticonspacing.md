---
title: Mensagem de LVM_SETICONSPACING (commctrl. h)
description: Define o espaçamento entre os ícones nos controles de exibição de lista que têm o \_ estilo de ícone LVS. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetIconSpacing do ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Controles de LVM_SETICONSPACING de mensagens do Windows
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
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824168"
---
# <a name="lvm_seticonspacing-message"></a>\_Mensagem SETICONSPACING LVM

Define o espaçamento entre os ícones nos controles de exibição de lista que têm o estilo de [**\_ ícone LVS**](list-view-window-styles.md) . Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetIconSpacing do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a distância, em pixels, para definir entre ícones no eixo x. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a distância, em pixels, para definir entre ícones no eixo y. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que contém a distância do eixo x anterior na palavra inferior e a distância anterior do eixo y na palavra alta.

## <a name="remarks"></a>Comentários

Os valores para *lParam* são relativos ao canto superior esquerdo de um bitmap de ícone. Portanto, para definir o espaçamento entre ícones que não se sobrepõem, os valores de *lParam* devem incluir o tamanho do ícone, além da quantidade de espaço vazio desejado entre os ícones. Os valores que não incluem a largura do ícone resultarão em sobreposições.

Ao definir o espaçamento de ícone, os valores de *lParam* devem ser definidos como 4 ou maiores. Valores menores não produzirão o layout desejado. Para redefinir os ícones para o espaçamento padrão, defina os valores de *lParam* como-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

