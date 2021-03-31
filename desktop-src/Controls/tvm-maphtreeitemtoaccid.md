---
title: Mensagem de TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Mapeia um HTREEITEM para uma ID de acessibilidade.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Controles de TVM_MAPHTREEITEMTOACCID de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085569"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>\_Mensagem TVM MAPHTREEITEMTOACCID

Mapeia um **HTREEITEM** para uma ID de acessibilidade.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM** que é mapeado para uma ID de acessibilidade.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma ID de acessibilidade.

## <a name="remarks"></a>Comentários

Quando você adiciona um item a um controle de exibição de árvore, um identificador **HTREEITEM** é retornado para identificar exclusivamente o item.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_MapHTREEITEMtoAccID TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





