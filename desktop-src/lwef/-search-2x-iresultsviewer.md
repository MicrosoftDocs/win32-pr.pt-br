---
title: Interface IResultsViewer (WdsSharedIDL.h)
description: Expõe métodos e propriedades para a exibição de resultados.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Interface IResultsViewer herdada Windows recursos de ambiente
- IResultsViewer interface Legacy Windows Environment Features , descrito
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1528f5d6da779e49836b75027845d40c76a2d948a9eb51e78b2addcefc75085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963766"
---
# <a name="iresultsviewer-interface"></a>Interface IResultsViewer

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Expõe métodos e propriedades para a exibição de resultados.

## <a name="members"></a>Membros

A interface **IResultsViewer** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultsViewer** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IResultsViewer** tem esses métodos.



| Método                                                   | Descrição                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Não implementado.<br/>                                                            |
| [**Goforward**](-search-2x-iresultsviewer-goforward.md) | Não implementado.<br/>                                                            |
| [**Atualizar**](-search-2x-iresultsviewer-refresh.md)     | Não implementado.<br/>                                                            |
| [**Stop**](-search-2x-iresultsviewer-stop.md)           | Não implementado.<br/>                                                            |
| [**Atualizar**](-search-2x-iresultsviewer-update.md)       | Aplica as alterações de consulta e navega a exibição para o novo conjunto de resultados.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IResultsViewer** tem essas propriedades.



| Propriedade                                                                            | Tipo de acesso           | Descrição                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Sumário**](-search-2x-iresultsviewer-contents.md)<br/>                   | Somente gravação<br/> | Essa propriedade rastreia o tipo do conteúdo que está sendo exibido na exibição de resultados. <br/>    |
| [**Displayname**](-search-2x-iresultsviewer-displayname.md)<br/>             | Somente leitura<br/>  | Nome de exibição localizado do tipo.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Somente gravação<br/> | Não implementado.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Leitura/gravação<br/> | Essa propriedade definirá ou retornará o nome do tipo pré-criado pelo qual filtrar os resultados.<br/> |
| [**Headerstyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Leitura/gravação<br/> | O estilo do header exibido na exibição.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Somente gravação<br/> | Isso retornará TRUE se a consulta de exibições tiver sido modificada e precisar de atualização. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Leitura/gravação<br/> | Essa propriedade definirá ou retornará o nome do armazenamento pelo o que filtrar os resultados.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Leitura/gravação<br/> | Controla o modo de exibição do painel de visualização.<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Somente gravação<br/> | Ao chamar a coleção de filtros de propriedade, ele retornará o seguinte:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define o texto da consulta atual.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Somente gravação<br/> | Não implementado.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Leitura/gravação<br/> | Essa propriedade definirá ou retornará a ordem das colunas pelas as que os resultados serão classificação. <br/>            |
| [**Sortproperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Leitura/gravação<br/> | Essa propriedade definirá ou retornará o IndexColumn da propriedade por onde classificar os resultados. <br/> |



 

## <a name="remarks"></a>Comentários

Esses métodos e propriedades são usados para manipular as informações exibidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

