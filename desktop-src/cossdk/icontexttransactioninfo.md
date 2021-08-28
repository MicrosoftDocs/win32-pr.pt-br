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
ms.openlocfilehash: be470d2a06d5dc284963e76ded188cb6a11fabd963b4f1186a3cee697bdfb6df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793446"
---
# <a name="icontexttransactioninfo-interface"></a>Interface IContextTransactionInfo

Fornece acesso a propriedades de objeto de contexto relacionadas a transações.

## <a name="when-to-implement"></a>Quando implementar

Você não deve implementar essa interface. A implementação padrão fornece funcionalidade completa.

## <a name="when-to-use"></a>Quando usar

Use essa interface para acessar propriedades de objeto de contexto relacionadas a transações.

## <a name="members"></a>Membros

A interface **IContextTransactionInfo** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextTransactionInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextTransactionInfo** tem esses métodos.



| Método                                                                                         | Descrição                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Recupera a transação ou o proxy de transação associado ao contexto atual, se for o caso.<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Recupera o nível de isolamento e o valor de tempo-máximo de uma transação que está hospedada no contexto de transação raiz.<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | Associa uma implementação [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) ao contexto atual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/> |



 

