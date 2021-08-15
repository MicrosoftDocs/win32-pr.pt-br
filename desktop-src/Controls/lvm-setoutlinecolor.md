---
title: LVM_SETOUTLINECOLOR mensagem (Commctrl.h)
description: Define a cor da borda de um controle de exibição de lista se o estilo de janela estendida LVS \_ EX \_ BORDERSELECT estiver definido.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db9f5d53339ecec19fd6f06fcabd3a0471b1c3a569e8856571a98a99675a232
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217386"
---
# <a name="lvm_setoutlinecolor-message"></a>Mensagem LVM \_ SETOUTLINECOLOR

Define a cor da borda de um controle de exibição de lista se o estilo de janela estendida [**LVS \_ EX \_ BORDERSELECT**](extended-list-view-styles.md) estiver definido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>**Estrutura COLORREF** que especifica a cor para definir a borda.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **a estrutura COLORREF** que contém a cor do contorno.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





