---
title: Mensagem de TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Mapas uma ID de acessibilidade a um HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- controles de Windows de mensagem de TVM_MAPACCIDTOHTREEITEM
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6481d8db806156d10536ac0ec7c66fdeb4693a1133365767b4c3dc37ad8420f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045796"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>\_Mensagem TVM MAPACCIDTOHTREEITEM

Mapas uma ID de acessibilidade a um **HTREEITEM**.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** que contém a ID de acessibilidade para mapear para um **HTREEITEM**. </dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o **HTREEITEM** ao qual a ID de acessibilidade especificada está mapeada.

## <a name="remarks"></a>Comentários

Quando você adiciona um item a um controle de exibição de árvore, um **HTREEITEM** retorna, que identifica exclusivamente o item.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_MapAccIDToHTREEITEM TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





