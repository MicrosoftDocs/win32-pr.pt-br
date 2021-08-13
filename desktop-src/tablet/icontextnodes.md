---
description: Contém uma coleção de objetos que implementam a interface IContextNode e que são o resultado de uma operação de análise de tinta.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interface IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e1cc15817fa36c8cecaf06c1da0fd8fb7dae77b77909f2e04b5ebaef8100d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266146"
---
# <a name="icontextnodes-interface"></a>Interface IContextNodes

Contém uma coleção de objetos que implementam a interface [**IContextNode**](icontextnode.md) e que são o resultado de uma operação de análise de tinta.

## <a name="members"></a>Membros

A interface **IContextNodes** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextNodes** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextNodes** tem esses métodos.



| Método                                                       | Descrição                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddContextNode**](icontextnodes-addcontextnode.md)       | Adiciona um objeto [**IContextNode**](icontextnode.md) a esta coleção. <br/>                                  |
| [**GetContextNode**](icontextnodes-getcontextnode.md)       | Recupera o objeto [**IContextNode**](icontextnode.md) no índice especificado dentro desta coleção. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Recupera o número de objetos [**IContextNode**](icontextnode.md) contidos nesta coleção. <br/>       |
| [**RemoveContextNode**](icontextnodes-removecontextnode.md) | Remove um objeto [**IContextNode**](icontextnode.md) desta coleção. <br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

