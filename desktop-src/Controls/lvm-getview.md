---
title: Mensagem de LVM_GETVIEW (commctrl. h)
description: Recupera a exibição atual de um controle de exibição de lista.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Controles de LVM_GETVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086157"
---
# <a name="lvm_getview-message"></a>\_Mensagem GETVIEW LVM

Recupera a exibição atual de um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **DWORD** que especifica a exibição atual.

## <a name="remarks"></a>Comentários

A seguir estão os valores para exibições.

-   \_detalhes da exibição de LV \_
-   \_ícone de exibição LV \_
-   \_lista de exibição de LV \_
-   \_SMALLICON de exibição LV \_
-   \_bloco de exibição LV \_

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





