---
description: Definindo os sinalizadores consistentes e feitos
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Definindo os sinalizadores consistentes e feitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518864efda3716ea9998ed306b0ca6901b70697f8cb3acabe813d3e2e3e0bcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500046"
---
# <a name="setting-the-consistent-and-done-flags"></a>Definindo os sinalizadores consistentes e feitos

Você pode definir os sinalizadores consistentes e feitos invocando métodos nas interfaces [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) ou [**IContextState.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) As estratégias usadas por essas duas interfaces diferem significativamente. **IObjectContext** tem quatro métodos que vinculam os sinalizadores consistentes e feitos em combinações exclusivas, enquanto **IContextState** tem dois métodos que permitem definir cada sinalizador independentemente. Os métodos de **IObjectContext** também são expostos por meio do [**objeto ObjectContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext)

Para controle independente de cada sinalizador, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) fornece um método para definir o sinalizador consistente como True ou False e um método para definir o sinalizador done como True ou False. Esses métodos são [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) e [**SetDeactivateOnReturn,**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn)respectivamente. A interface **IContextState** também inclui métodos para recuperar o valor atual de cada sinalizador.

Quando você definir o valor do método [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) como TxCommit, o COM+ verificará a presença de uma transação. Se o COM+ não detectar uma transação, ele gerará um erro que você pode capturar em um arquivo de log. Por exemplo, suponha que alguém configure inadvertidamente o atributo de transação do componente como Sem Suporte, mas você esperava que ele fosse definido como Obrigatório. Ao definir **SetMyTransactionVote** = TxCommit, você pode identificar o conflito e tomar medidas.

A tabela a seguir descreve as chamadas de método que podem ser usadas para definir os sinalizadores consistentes e feitos.



| Sinalizador consistente  | Sinalizador done        | Método IObjectContext                                            | Métodos IContextState                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verdadeiro<br/>  | Falso<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/> |
| Falso<br/> | Falso<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/>  |
| Falso<br/> | True<br/>  | [**Setabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True<br/>   |
| True<br/>  | True<br/>  | [**Setcomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True              |



 

> [!Note]  
> A propriedade auto-done, que é definida no nível do método, pode afetar como os sinalizadores consistentes e feitos são definidos. Para obter mais informações sobre a propriedade auto-done, consulte [Habilitando o auto-done para um](enabling-auto-done-for-a-method.md) método e [Definindo o bit feito.](setting-the-done-bit.md)

 

 

 




