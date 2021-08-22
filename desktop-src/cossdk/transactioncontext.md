---
description: Cria um objeto transacional genérico que inicia uma transação.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Classe TransactionContext (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: aa0a90cee2b0af7d5ebe3679dca46aa04c6326fb5fd62fe5f57699d610b9efe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678146"
---
# <a name="transactioncontext-class"></a>Classe TransactionContext

Cria um objeto transacional genérico que inicia uma transação. Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e fazer commit ou anular explicitamente a transação.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ TransactionContext                          |
| ProgID     | L"TxCTx.TransactionContext"                        |
| Interfaces | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Quando usar

Um cliente não transacional usa essa classe para iniciar uma transação. Usando os métodos dessa classe, o cliente pode chamar objetos COM adicionais que, se configurados para participar de uma transação, são executados dentro do limite de transação do objeto de contexto de transação. Com base em sua lógica de negócios, o cliente pode explicitamente fazer commit ou anular a transação.

A **classe TransactionContext** limita a reutilização da lógica de negócios que conduz a transação. Por esse motivo, é recomendável que os objetos instautados da **classe TransactionContext** sejam usados com moderação.

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à Biblioteca de Tipos de Serviços COM+. Um objeto TransactionContext pode ser declarado usando "COMSVCSLib.TransactionContext" como o nome da classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Configurando transações](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




