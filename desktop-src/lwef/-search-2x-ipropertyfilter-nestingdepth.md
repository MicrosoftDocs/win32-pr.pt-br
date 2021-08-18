---
title: Propriedade IPropertyFilter NestingDepth (WdsSharedIDL.h)
description: Filtra a profundidade em um conjunto aninhado de parênteses.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Propriedade NestingDepth Herdada Windows Recursos de Ambiente
- Propriedade NestingDepth Herdada Windows Recursos de Ambiente, interface IPropertyFilter
- Interface IPropertyFilter Herdada Windows recursos de ambiente, propriedade NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2499d7a3d5505f4cb428cbc8831ec0ea4e0a71843693f5a8ba1250995071df32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481204"
---
# <a name="ipropertyfilternestingdepth-property"></a>Propriedade IPropertyFilter::NestingDepth

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Filtra a profundidade em um conjunto aninhado de parênteses.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a>Valor da propriedade

Define o número que indica a profundidade dos parênteses aninhados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





