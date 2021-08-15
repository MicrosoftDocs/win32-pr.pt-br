---
description: Define métodos para obter informações sobre as propriedades de um item de pesquisa. Essa interface tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.
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
ms.openlocfilehash: 2657fea53c4e7021e17df4b74cc210bd8547180566ff579524f85b7663a0c247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226556"
---
# <a name="iitempropertybag-interface"></a>Interface IItemPropertyBag

Define métodos para obter informações sobre as propriedades de um item de pesquisa. Essa interface tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

## <a name="members"></a>Membros

A interface **IItemPropertyBag** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IItemPropertyBag** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IItemPropertyBag** tem esses métodos.



| Método                                                      | Descrição                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Obtém uma contagem do número de propriedades no pacote de propriedades.<br/>                     |
| [**Getpropertyinfo**](iitempropertybag-getpropertyinfo.md) | Obtém as informações necessárias para ler ou salvar as propriedades no pacote de propriedades.<br/> |
| [**Ler**](iitempropertybag-read.md)                       | Faz com que uma ou mais propriedades sejam lidas do pacote de propriedades.<br/>                   |
| [**Gravar**](iitempropertybag-write.md)                     | Faz com que uma ou mais propriedades sejam salvas no pacote de propriedades.<br/>                  |



 

## <a name="remarks"></a>Comentários

A interface **IItemPropertyBag** tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

Para visualizar anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **IItemPropertyBag** e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) as estruturas [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>          |



 

 
