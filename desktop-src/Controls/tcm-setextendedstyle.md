---
title: Mensagem de TCM_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos que serão usados pelo controle da guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ setextendedattribute.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Controles de TCM_SETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009390"
---
# <a name="tcm_setextendedstyle-message"></a>Mensagem do TCM \_ SETextendedattribute

Define os estilos estendidos que serão usados pelo controle da guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor **DWORD** que indica quais estilos em *lParam* devem ser afetados. Somente os estilos estendidos em *wParam* serão alterados. Todos os outros estilos serão mantidos como estão. Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica os estilos de controle da guia estendida. Esse valor é uma combinação de [estilos estendidos](tab-control-extended-styles.md)de controle de guia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que contém os estilos estendidos do controle de guia anterior.

## <a name="remarks"></a>Comentários

O parâmetro *wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro. Por exemplo, se você passar [**TCS \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) para *wParam* e 0 para *lParam*, o estilo **TCS \_ ex \_ FLATSEPARATORS** será limpo, mas todos os outros estilos permanecerão os mesmos.

Por motivos de compatibilidade com versões anteriores, a macro [**TabCtrl \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) não foi atualizada para usar *dwExMask*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TCM \_ GETextendedattribute**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





