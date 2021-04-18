---
description: Representa uma relação entre dois objetos IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interface IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772576"
---
# <a name="icontextlink-interface"></a>Interface IContextLink

Representa uma relação entre dois objetos [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Membros

A interface **IContextLink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextLink** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextLink** tem esses métodos.



| Método                                                                  | Descrição                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Recupera o tipo de relação que esse **IContextLink** representa.<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Recupera o objeto [**IContextNode**](icontextnode.md) que é o destino para este **IContextLink**.<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Recupera o objeto [**IContextNode**](icontextnode.md) que é a origem para este **IContextLink**.<br/>      |



 

## <a name="remarks"></a>Comentários

Veja a seguir um exemplo de uma relação representada por um objeto **IContextLink** :

-   Quando um nó AnalysisHint é usado na análise de tinta, a operação de análise de tinta cria um objeto **IContextLink** do tipo AnalysisHint entre o nó de dica de análise e o nó que contém a gravação dentro da área da dica. O nó de origem é o nó de dica de análise e o nó de destino é o nó que contém a gravação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> </dl>

 

