---
title: Interface IPropertyFilter (WdsSharedIDL.h)
description: Expõe as propriedades usadas para filtrar a consulta.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Interface IPropertyFilter herdado Windows ambiente
- Interface IPropertyFilter Herdado Windows Recursos de Ambiente , descrito
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5bc406661492702e4a012cab58a2e0a3e08507aeaa13d10b010f14ce31e6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481090"
---
# <a name="ipropertyfilter-interface"></a>Interface IPropertyFilter

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Expõe as propriedades usadas para filtrar a consulta.

## <a name="members"></a>Membros

A interface **IPropertyFilter** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilter** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IPropertyFilter** tem essas propriedades.



| Propriedade                                                                                      | Tipo de acesso           | Description                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Leitura/gravação<br/> | Nome da coluna indexada da propriedade pela a ser filtrada. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Leitura/gravação<br/> | Operador lógico a ser usado ao aplicar o filtro. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Leitura/gravação<br/> | Filtra a profundidade em um conjunto aninhado de parênteses. <br/> |
| [**IPropertyFilter::Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Leitura/gravação<br/> | Texto do filtro. <br/>                               |
| [**IPropertyFilter::UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Leitura/gravação<br/> | UID para a propriedade por a ser filtrada. <br/>                 |



 

## <a name="remarks"></a>Comentários

Essas propriedades são usadas para filtrar a consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

