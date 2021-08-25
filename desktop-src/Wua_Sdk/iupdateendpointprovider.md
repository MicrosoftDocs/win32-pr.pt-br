---
description: Contém o método usado para obter um ponto de extremidade que é usado para se conectar a um serviço.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interface IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896836"
---
# <a name="iupdateendpointprovider-interface"></a>Interface IUpdateEndpointProvider

Contém o método usado para obter um ponto de extremidade que é usado para se conectar a um serviço. Essa interface é implementada durante a gravação de um provedor de ponto de extremidade.

## <a name="members"></a>Membros

A interface **IUpdateEndpointProvider** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointProvider** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUpdateEndpointProvider** tem esses métodos.



| Método                                                                       | Descrição                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Solicita um ponto de extremidade que é usado para se conectar a um serviço.<br/> |



 

## <a name="remarks"></a>Comentários

O WUA chama o método [**getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) para iniciar o processo de negociação. Quando a chamada é feita, o WUA passa nos tipos de token registrados e a implementação dessa interface retorna os tipos de token que ele prefere usar.

 

 
