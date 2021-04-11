---
title: Interface IPropertyFilterCollection (WdsSharedIDL. h)
description: Expõe as propriedades da coleção retornada com base na consulta enviada.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, descritos
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
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295819"
---
# <a name="ipropertyfiltercollection-interface"></a>Interface IPropertyFilterCollection

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe as propriedades da coleção retornada com base na consulta enviada.

## <a name="members"></a>Membros

A interface **IPropertyFilterCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilterCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IPropertyFilterCollection** tem essas propriedades.



| Propriedade                                                                         | Tipo de acesso           | Descrição                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**Item**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Somente leitura<br/>  | Adiciona um novo filtro à coleção. <br/>             |
| [**formatação**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Somente gravação<br/> | Limpa a coleção. <br/>                           |
| [**Contar**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Somente leitura<br/>  | Número de filtros na coleção. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Leitura/gravação<br/> | Retorna um filtro específico dentro da coleção. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Somente gravação<br/> | Remove um filtro específico para a coleção. <br/>     |



 

## <a name="remarks"></a>Comentários

Essas propriedades são usadas para filtrar a coleção retornada pela consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

