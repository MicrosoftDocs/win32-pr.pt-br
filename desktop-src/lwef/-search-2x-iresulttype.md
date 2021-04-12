---
title: Interface IResultType (WdsSharedIDL. h)
description: Expõe informações de tipo de propriedade.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Recursos do ambiente Windows herdado da interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, descritos
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454950"
---
# <a name="iresulttype-interface"></a>Interface IResultType

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe informações de tipo de propriedade.

## <a name="members"></a>Membros

A interface **IResultType** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultType** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IResultType** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso           | Descrição                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresulttype-displayname.md)<br/>     | Somente leitura<br/>  | Nome de exibição localizado do tipo:<br/>                                        |
| [**GetProperty**](-search-2x-iresulttype-getproperty.md)<br/>     | Leitura/gravação<br/> | Esta propriedade contém informações de propriedade especificadas. <br/>                    |
| [**PreceivedType**](-search-2x-iresulttype-preceivedtype.md)<br/> | Somente leitura<br/>  | Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice. <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | Somente leitura<br/>  | Essa propriedade contém o número de propriedades expostas pelo tipo. <br/>      |
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | Somente leitura<br/>  | Essa propriedade contém o identificador exclusivo para o tipo. <br/>                |



 

## <a name="remarks"></a>Comentários

Esses métodos expõem os tipos de informações retornados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

