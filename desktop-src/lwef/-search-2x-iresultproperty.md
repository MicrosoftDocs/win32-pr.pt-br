---
title: Interface IResultProperty (WdsSharedIDL.h)
description: Expõe propriedades de resultado.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Interface IResultProperty Herdado Windows ambiente
- IResultProperty interface Legacy Windows Environment Features , descrito
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
ms.openlocfilehash: efba214aaaadec2cfad52db02f9f4f18d289b0b3ee9df37ee60295d5499241e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754579"
---
# <a name="iresultproperty-interface"></a>Interface IResultProperty

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Expõe propriedades de resultado.

## <a name="members"></a>Membros

A interface **IResultProperty** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultProperty** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IResultProperty** tem esses métodos.



| Método                                                    | Descrição                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Não implementado.<br/> |
| [**Goforward**](-search-2x-iresultproperty-goforward.md) | Não implementado.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IResultProperty** tem essas propriedades.



| Propriedade                                                                   | Tipo de acesso          | Descrição                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Datatype**](-search-2x-iresultproperty-datatype.md)<br/>         | Somente leitura<br/> | Um tipo de dados de propriedades. <br/>                   |
| [**Displayname**](-search-2x-iresultproperty-displayname.md)<br/>   | Somente leitura<br/> | Nome de exibição localizado da propriedade. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Somente leitura<br/> | Visabilidade da propriedade. <br/>               |
| [**Dica**](-search-2x-iresultproperty-hint.md)<br/>                 | Somente leitura<br/> | Valor especial usado para auxiliar na recuperação de dados. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Somente leitura<br/> | Nome da coluna propriedades no índice. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Somente leitura<br/> | Identificador exclusivo para a propriedade. <br/>       |



 

## <a name="remarks"></a>Comentários

Esses são os itens que retornam propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

