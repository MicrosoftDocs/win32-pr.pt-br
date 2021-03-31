---
description: Contém uma coleção de objetos que implementam a interface IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interface IContextLinks (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920957"
---
# <a name="icontextlinks-interface"></a>Interface IContextLinks

Contém uma coleção de objetos que implementam a interface [**IContextLink**](icontextlink.md) .

## <a name="members"></a>Membros

A interface **IContextLinks** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextLinks** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextLinks** tem esses métodos.



| Método                                                 | Descrição                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**GetContextLink**](icontextlinks-getcontextlink.md) | Recupera o [**IContextLink**](icontextlink.md) no índice especificado.<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | Recupera o número de objetos [**IContextLink**](icontextlink.md) nesta coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Normalmente, isso é acessado por meio do método [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

