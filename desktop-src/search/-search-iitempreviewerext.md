---
description: Fornece métodos para fornecer configurações do navegador. A interface IItemPreviewerExt tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interface IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920763"
---
# <a name="iitempreviewerext-interface"></a>Interface IItemPreviewerExt

Fornece métodos para fornecer configurações do navegador. A interface **IItemPreviewerExt** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

## <a name="members"></a>Membros

A interface **IItemPreviewerExt** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPreviewerExt** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IItemPreviewerExt** tem esses métodos.



| Método                                                                               | Descrição                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)               | Permite a extensão para o conteúdo avançado de uma propriedade. <br/>                            |
| [**GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)                   | Obtém uma parte do corpo relacionado para inserir no fluxo de saída de MHTML.<br/>              |
| [**ProcessTransformCommand**](-search-iitempreviewerext-processtransformcommand.md) | Permite o processamento de um comando de transformação encontrado em um modelo de visualização.<br/> |
| [**SuggestBrowserPolicy**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | Sugere a política de segurança a ser aplicada ao navegador.<br/>                        |



 

## <a name="remarks"></a>Comentários

A interface **IItemPreviewerExt** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **IItemPreviewerExt** e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
