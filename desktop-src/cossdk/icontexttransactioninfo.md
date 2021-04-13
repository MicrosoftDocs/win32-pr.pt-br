---
description: Fornece acesso a propriedades de objeto de contexto relacionadas a transações.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interface IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457054"
---
# <a name="icontexttransactioninfo-interface"></a>Interface IContextTransactionInfo

Fornece acesso a propriedades de objeto de contexto relacionadas a transações.

## <a name="when-to-implement"></a>Quando implementar

Você não deve implementar essa interface. A implementação padrão fornece a funcionalidade completa.

## <a name="when-to-use"></a>Quando usar

Use essa interface para acessar propriedades de objeto de contexto relacionadas a transações.

## <a name="members"></a>Membros

A interface **IContextTransactionInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextTransactionInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextTransactionInfo** tem esses métodos.



| Método                                                                                         | Descrição                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Recupera a transação ou o proxy de transação que está associado ao contexto atual, se houver.<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Recupera o nível de isolamento e o valor de tempo limite de uma transação hospedada no contexto de transação raiz.<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | Associa uma implementação de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) com o contexto atual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/> |



 

