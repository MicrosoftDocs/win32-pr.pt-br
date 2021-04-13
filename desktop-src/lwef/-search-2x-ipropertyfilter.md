---
title: Interface IPropertyFilter (WdsSharedIDL. h)
description: Expõe as propriedades usadas para filtrar a consulta.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Recursos do ambiente Windows herdado da interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, descritos
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
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499552"
---
# <a name="ipropertyfilter-interface"></a>Interface IPropertyFilter

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe as propriedades usadas para filtrar a consulta.

## <a name="members"></a>Membros

A interface **IPropertyFilter** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilter** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IPropertyFilter** tem essas propriedades.



| Propriedade                                                                                      | Tipo de acesso           | Descrição                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Leitura/gravação<br/> | Nome da coluna indexada da propriedade pela qual filtrar. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Leitura/gravação<br/> | Operador lógico a ser usado ao aplicar o filtro. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Leitura/gravação<br/> | Profundidade de filtros em um conjunto aninhado de parênteses. <br/> |
| [**IPropertyFilter:: texto**](-search-2x-ipropertyfilter-text.md)<br/>                   | Leitura/gravação<br/> | Texto do filtro. <br/>                               |
| [**IPropertyFilter:: UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Leitura/gravação<br/> | UID da propriedade pela qual filtrar. <br/>                 |



 

## <a name="remarks"></a>Comentários

Essas propriedades são usadas para filtrar a consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

