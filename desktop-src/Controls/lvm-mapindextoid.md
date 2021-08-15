---
title: Mensagem de LVM_MAPINDEXTOID (commctrl. h)
description: Mapas o índice de um item a uma ID exclusiva.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- controles de Windows de mensagem de LVM_MAPINDEXTOID
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254bfff0ee1598b0657b44a967b9e1331b076a462c8703855c5dd23109a8835d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958145"
---
# <a name="lvm_mapindextoid-message"></a>\_Mensagem MAPINDEXTOID LVM

Mapas o índice de um item a uma ID exclusiva.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de um item.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma ID exclusiva.

## <a name="remarks"></a>Comentários

Controles de exibição de lista controlam internamente os itens por índice. Isso pode apresentar problemas porque os índices podem ser alterados durante o tempo de vida do controle.

O controle de exibição de lista pode marcar um item com uma ID quando o item é criado. Você pode usar essa ID para garantir a exclusividade durante o tempo de vida do controle de exibição de lista.

Para identificar exclusivamente um item, pegue o índice que é retornado de uma chamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chame o **LVM \_ MAPINDEXTOID**. O valor de retorno é uma ID exclusiva.

> [!Note]  
> Em um ambiente multi-threaded, o índice só é garantido no thread que hospeda o controle de exibição de lista, não em threads em segundo plano.

 

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

