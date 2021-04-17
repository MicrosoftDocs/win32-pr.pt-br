---
title: Interface IResultProperty (WdsSharedIDL. h)
description: Expõe as propriedades de resultado.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Recursos do ambiente Windows herdado da interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, descritos
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760993"
---
# <a name="iresultproperty-interface"></a>Interface IResultProperty

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe as propriedades de resultado.

## <a name="members"></a>Membros

A interface **IResultProperty** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultProperty** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IResultProperty** tem esses métodos.



| Método                                                    | Descrição                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Não implementado.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Não implementado.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IResultProperty** tem essas propriedades.



| Propriedade                                                                   | Tipo de acesso          | Descrição                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Tipo de dados**](-search-2x-iresultproperty-datatype.md)<br/>         | Somente leitura<br/> | Um tipo de dados de propriedades. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Somente leitura<br/> | Nome de exibição localizado da propriedade. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Somente leitura<br/> | Visability da propriedade. <br/>               |
| [**Hint**](-search-2x-iresultproperty-hint.md)<br/>                 | Somente leitura<br/> | Valor especial usado para auxiliar a recuperação de dados. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Somente leitura<br/> | Nome da coluna de propriedades no índice. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Somente leitura<br/> | Identificador exclusivo da propriedade. <br/>       |



 

## <a name="remarks"></a>Comentários

Esses são os itens que retornam propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

