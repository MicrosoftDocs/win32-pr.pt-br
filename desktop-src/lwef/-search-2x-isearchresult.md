---
title: Interface ISearchResult (WdsSharedIDL. h)
description: Expõe informações e propriedades referentes ao conjunto de resultados.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- recursos de ambiente de Windows herdado da interface ISearchResult
- recursos de ambiente herdado Windows da interface ISearchResult, descritos
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd15db1340b28c8ac273746a64a5aee8c4b3235155d948692ffcc16582ac4549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963516"
---
# <a name="isearchresult-interface"></a>Interface ISearchResult

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe informações e propriedades referentes ao conjunto de resultados.

## <a name="members"></a>Membros

A interface **ISearchResult** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISearchResult** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISearchResult** tem esses métodos.



| Método                                                            | Descrição                 |
|:------------------------------------------------------------------|:----------------------------|
| [**Disponibilidade**](-search-2x-isearchresult-availability.md)     | Não implementado.<br/> |
| [**Doverbs**](-search-2x-isearchresult-doverb.md)                 | Não implementado.<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | Não implementado.<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | Não implementado.<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | Não implementado.<br/> |
| [**Getverbs**](-search-2x-isearchresult-getverb.md)               | Não implementado.<br/> |
| [**IconCount**](-search-2x-isearchresult-iconcount.md)           | Não implementado.<br/> |
| [**Índice**](-search-2x-isearchresult-index.md)                   | Não implementado.<br/> |
| [**LoadState**](-search-2x-isearchresult-loadstate.md)           | Não implementado.<br/> |
| [**Pré-visualizador**](-search-2x-isearchresult-previewer.md)           | Não implementado.<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | Não implementado.<br/> |
| [**Miniaturastate**](-search-2x-isearchresult-thumbnailstate.md) | Não implementado.<br/> |
| [**Tipo**](-search-2x-isearchresult-type.md)                     | Não implementado.<br/> |
| [**VerbCount**](-search-2x-isearchresult-verbcount.md)           | Não implementado.<br/> |



 

## <a name="remarks"></a>Comentários

Esses métodos expõem propriedades e ações aplicáveis ao conjunto de resultados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de desktop (WDS) 3,0<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

