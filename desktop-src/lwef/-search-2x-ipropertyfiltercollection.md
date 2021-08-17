---
title: Interface IPropertyFilterCollection (WdsSharedIDL.h)
description: Expõe propriedades da coleção retornada com base na consulta enviada.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Interface IPropertyFilterCollection Herdado Windows ambiente
- IPropertyFilterCollection interface Legacy Windows Environment Features , descrito
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69fb2f7ce6e100c74046f3402eee3385108723202fbaa6dce01e888bffef4b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349976"
---
# <a name="ipropertyfiltercollection-interface"></a>Interface IPropertyFilterCollection

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Expõe propriedades da coleção retornada com base na consulta enviada.

## <a name="members"></a>Membros

A interface **IPropertyFilterCollection** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilterCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IPropertyFilterCollection** tem essas propriedades.



| Propriedade                                                                         | Tipo de acesso           | Descrição                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**Additem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Somente leitura<br/>  | Adiciona um novo filtro à coleção. <br/>             |
| [**Claro**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Somente gravação<br/> | Limpa a coleção. <br/>                           |
| [**Contagem**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Somente leitura<br/>  | Número de filtros na coleção. <br/>             |
| [**Getitem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Leitura/gravação<br/> | Retorna um filtro específico dentro da coleção. <br/> |
| [**Removeitem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Somente gravação<br/> | Remove um filtro específico para a coleção. <br/>     |



 

## <a name="remarks"></a>Comentários

Essas propriedades são usadas para filtrar a coleção retornada pela consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

