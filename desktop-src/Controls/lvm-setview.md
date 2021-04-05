---
title: Mensagem de LVM_SETVIEW (commctrl. h)
description: Define a exibição de um controle de exibição de lista.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Controles de LVM_SETVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086150"
---
# <a name="lvm_setview-message"></a>Mensagem do LVM \_ SETview

Define a exibição de um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD** que especifica a exibição.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará 1 se for bem-sucedido ou-1 caso contrário. Por exemplo,-1 será retornado se a exibição for inválida.

## <a name="remarks"></a>Comentários

A seguir estão os valores para exibições.

-   \_detalhes da exibição de LV \_
-   \_ícone de exibição LV \_
-   \_lista de exibição de LV \_
-   \_SMALLICON de exibição LV \_
-   \_bloco de exibição LV \_

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comctl32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





