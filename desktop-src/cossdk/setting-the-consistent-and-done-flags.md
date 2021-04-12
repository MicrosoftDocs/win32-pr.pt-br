---
description: Definindo os sinalizadores consistentes e concluídos
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Definindo os sinalizadores consistentes e concluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd45d457828a222ce7f4ccbdc0080001b0f0b55f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456950"
---
# <a name="setting-the-consistent-and-done-flags"></a>Definindo os sinalizadores consistentes e concluídos

Você define os sinalizadores consistentes e concluídos invocando métodos nas interfaces [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) ou [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) . As estratégias usadas por essas duas interfaces diferem significativamente. O **IObjectContext** tem quatro métodos que associam os sinalizadores consistentes e concluídos em combinações exclusivas, enquanto o **IContextState** tem dois métodos que permitem que você defina cada sinalizador de forma independente. Os métodos de **IObjectContext** também são expostos por meio do objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Para o controle independente de cada sinalizador, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) fornece um método para definir o sinalizador consistente como true ou false e um método para definir o sinalizador Done como true ou false. Esses métodos são [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) e [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn), respectivamente. A interface **IContextState** também inclui métodos para recuperar o valor atual de cada sinalizador.

Quando você define o valor do método [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) como TxCommit, o com+ verifica a presença de uma transação. Se o COM+ não detectar uma transação, ele gerará um erro que poderá ser capturado em um arquivo de log. Por exemplo, suponha que alguém configure inadvertidamente o atributo de transação do componente como sem suporte, mas você esperava que ele seja definido como Required. Ao definir **SetMyTransactionVote** = TxCommit, você pode identificar o conflito e executar a ação.

A tabela a seguir descreve as chamadas de método que podem ser usadas para definir os sinalizadores consistentes e concluídos.



| Sinalizador consistente  | Sinalizador concluído        | Método IObjectContext                                            | Métodos IContextState                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| True<br/>  | Falso<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/> |
| Falso<br/> | Falso<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/>  |
| Falso<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true              |



 

> [!Note]  
> A propriedade auto-Done, que é definida no nível do método, pode afetar como os sinalizadores consistentes e concluídos são definidos. Para obter mais informações sobre a propriedade auto-Done, consulte [habilitando auto-pronto para um método](enabling-auto-done-for-a-method.md) e [definindo o bit feito](setting-the-done-bit.md).

 

 

 




