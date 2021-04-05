---
description: Fornece métodos que definem a interação entre uma interface do usuário e os objetos de namespace de pesquisa criados pelo indexador.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interface ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370622"
---
# <a name="isearchitem-interface"></a>Interface ISearchItem

Fornece métodos que definem a interação entre uma interface do usuário e os objetos de namespace de pesquisa criados pelo indexador.

## <a name="members"></a>Membros

A interface **ISearchItem** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchItem** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISearchItem** tem esses métodos.



| Método                                                         | Descrição                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Obtém o objeto **ISearchItem** se a URL representa uma fonte de dados do Shell real (também conhecida como extensão de namespace do Shell).<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Obtém o objeto da interface do usuário (UI) de **ISearchItem**.<br/>                                                                        |



 

## <a name="remarks"></a>Comentários

O [**ISearchItem:: GetParentFolder**](-search-isearchitem-getparentfolder.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usado.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **ISearchItem** e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
