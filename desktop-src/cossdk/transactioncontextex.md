---
description: Cria um objeto transacional genérico que inicia uma transação. Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e confirmar explicitamente ou anular a transação.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Classe TransactionContextEx (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646484"
---
# <a name="transactioncontextex-class"></a>Classe TransactionContextEx

Cria um objeto transacional genérico que inicia uma transação. Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e confirmar explicitamente ou anular a transação.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|--------------------------------------------------------|
| CLSID      | \_TRANSACTIONCONTEXTEX CLSID                            |
| ProgID     | L "TxCTx. TransactionContextEx"                          |
| Interfaces | [**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>Quando usar

Um cliente não transacional usa essa classe para iniciar uma transação. Usando os métodos dessa classe, o cliente pode chamar objetos COM adicionais que, se configurados para participar de uma transação, são executados dentro do limite de transação do objeto de contexto de transação. Com base em sua lógica de negócios, o cliente pode confirmar ou anular explicitamente a transação.

A classe **TransactionContextEx** limita a reutilização da lógica de negócios que orienta a transação. Por esse motivo, é recomendável que os objetos instanciados da classe **TransactionContextEx** sejam usados com moderação.

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

A classe **TransactionContextEx** não foi projetada para ser usada em Visual Basic. Em vez disso, use a classe [**TransactionContext**](transactioncontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Configurando transações](configuring-transactions.md)
</dt> <dt>

[**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**TransactionContext**](transactioncontext.md)
</dt> </dl>

 

 




