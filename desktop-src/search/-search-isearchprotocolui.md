---
description: Fornece um método para invocar objetos ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interface ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4794c0a2de43c08645af5ea7d44d0dbd872fe6fc88c33f5fcdb830955fc594be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463011"
---
# <a name="isearchprotocolui-interface"></a>Interface ISearchProtocolUI

Fornece um método para invocar objetos [**ISearchItem**](-search-isearchitem.md) . Os métodos nessa interface são chamados pelo host de protocolo ao processar URLs do gatherer. O manipulador de protocolo implementa o protocolo para acessar uma fonte de conteúdo em seu formato nativo, e essa interface implementa um manipulador de protocolo personalizado para expandir as fontes de dados que podem ser indexadas.

## <a name="members"></a>Membros

A interface **ISearchProtocolUI** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchProtocolUI** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISearchProtocolUI** tem esses métodos.



| Método                                                                       | Descrição                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Obtém o item de pesquisa para os dados especificados. Esse método é chamado uma vez para cada URL processada pelo gatherer e recupera um ponteiro para o objeto [**ISearchItem**](-search-isearchitem.md) . <br/> |



 

## <a name="remarks"></a>Comentários

a interface **ISearchProtocolUI** tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.

para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **ISearchProtocolUI** e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**linkid**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de desktop (WDS) 3,0<br/>          |



 

 
