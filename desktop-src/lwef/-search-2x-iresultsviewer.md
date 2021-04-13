---
title: Interface IResultsViewer (WdsSharedIDL. h)
description: Expõe métodos e propriedades para a exibição de resultados.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Recursos do ambiente Windows herdado da interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, descritos
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
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499490"
---
# <a name="iresultsviewer-interface"></a>Interface IResultsViewer

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe métodos e propriedades para a exibição de resultados.

## <a name="members"></a>Membros

A interface **IResultsViewer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultsViewer** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IResultsViewer** tem esses métodos.



| Método                                                   | Descrição                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Não implementado.<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | Não implementado.<br/>                                                            |
| [**Atualizar**](-search-2x-iresultsviewer-refresh.md)     | Não implementado.<br/>                                                            |
| [**Stop**](-search-2x-iresultsviewer-stop.md)           | Não implementado.<br/>                                                            |
| [**Cumulativo**](-search-2x-iresultsviewer-update.md)       | Aplica qualquer alteração de consulta e navega a exibição para o novo conjunto de resultados.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IResultsViewer** tem essas propriedades.



| Propriedade                                                                            | Tipo de acesso           | Descrição                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Sumário**](-search-2x-iresultsviewer-contents.md)<br/>                   | Somente gravação<br/> | Essa propriedade controla o tipo do conteúdo que está sendo exibido no modo de exibição de resultados. <br/>    |
| [**DisplayName**](-search-2x-iresultsviewer-displayname.md)<br/>             | Somente leitura<br/>  | Nome de exibição localizado do tipo.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Somente gravação<br/> | Não implementado.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Leitura/gravação<br/> | Essa propriedade definirá ou retornará o nome do tipo preceived para filtrar os resultados por.<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Leitura/gravação<br/> | O estilo do cabeçalho exibido na exibição.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Somente gravação<br/> | Isso retornará TRUE se a consulta views tiver sido modificada e precisar de atualização. <br/>           |
| [**Repositório de armazenamento**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Leitura/gravação<br/> | Essa propriedade definirá ou retornará o nome do repositório para filtrar os resultados por.<br/>          |
| [**Modo de exibição**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Leitura/gravação<br/> | Controla o modo de exibição do painel de visualização.<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Somente gravação<br/> | Ao chamar a coleção de filtros de propriedade, ele retornará o seguinte:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define o texto da consulta atual.<br/>                                                  |
| [**Resultstyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Somente gravação<br/> | Não implementado.<br/>                                                                      |
| [**SortOrderproperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Leitura/gravação<br/> | Essa propriedade definirá ou retornará a ordem das colunas para classificar os resultados por. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Leitura/gravação<br/> | Essa propriedade irá definir ou retornar o IndexColumn da propriedade para classificar os resultados por. <br/> |



 

## <a name="remarks"></a>Comentários

Esses métodos e propriedades são usados para manipular as informações exibidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

