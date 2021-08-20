---
description: Contém uma coleção de objetos que implementam a interface IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interface IContextLinks (IACom.h)
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
ms.openlocfilehash: 44eb7117fe3b01b3e31829222c6ab3f601d5bbbec8ea0591a9f80d087dcaee22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008476"
---
# <a name="icontextlinks-interface"></a>Interface IContextLinks

Contém uma coleção de objetos que implementam a interface [**IContextLink.**](icontextlink.md)

## <a name="members"></a>Membros

A interface **IContextLinks** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextLinks** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextLinks** tem esses métodos.



| Método                                                 | Descrição                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**GetContextLink**](icontextlinks-getcontextlink.md) | Recupera o [**IContextLink**](icontextlink.md) no índice especificado.<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | Recupera o número de [**objetos IContextLink**](icontextlink.md) nesta coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Isso geralmente é acessado por [**meio do método IContextNode::GetContextLinks.**](icontextnode-getcontextlinks.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
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

 

