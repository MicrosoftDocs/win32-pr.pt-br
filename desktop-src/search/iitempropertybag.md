---
description: Define métodos para obter informações sobre as propriedades de um item de pesquisa. Essa interface tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interface IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090048"
---
# <a name="iitempropertybag-interface"></a>Interface IItemPropertyBag

Define métodos para obter informações sobre as propriedades de um item de pesquisa. Essa interface tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.

## <a name="members"></a>Membros

A interface **IItemPropertyBag** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPropertyBag** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IItemPropertyBag** tem esses métodos.



| Método                                                      | Descrição                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Contarproperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Obtém uma contagem do número de propriedades no recipiente de propriedades.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Obtém as informações necessárias para ler ou salvar as propriedades no recipiente de propriedades.<br/> |
| [**Ler**](iitempropertybag-read.md)                       | Faz com que uma ou mais propriedades sejam lidas do recipiente de propriedades.<br/>                   |
| [**Gravar**](iitempropertybag-write.md)                     | Faz com que uma ou mais propriedades sejam salvas no recipiente de propriedades.<br/>                  |



 

## <a name="remarks"></a>Comentários

A interface **IItemPropertyBag** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **IItemPropertyBag** e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISEARCHITEM**](-search-isearchitem.md) , as estruturas [**LINKINFO**](-search-linkinfo.md) e [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
