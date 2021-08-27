---
description: Se você estiver escrevendo um serviço ou componente e precisar usar serviços transacionais ou se precisar monitorar o estado de uma transação de kernel, precisará criar um RM (gerenciador de recursos).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escrevendo um Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b1443bef61f56a14779612a6275aacbd65e344d7294325bd87b953795f0f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086446"
---
# <a name="writing-a-resource-manager"></a>Escrevendo um Resource Manager

Se você estiver escrevendo um serviço ou componente e precisar usar serviços transacionais ou se precisar monitorar o estado de uma transação de kernel, precisará criar um RM (gerenciador de recursos).

Para escrever um gerenciador de recursos, você deve criar vários objetos de kernel. Os objetos que um RM usa são:

-   Objetos do Gerenciador de Transações (TM)
-   Resource Manager objetos
-   Objetos de inscrever-se

Primeiro, crie um objeto TM. Há dois tipos de TMs:

-   Volátil – esses TMs não têm um log e não podem recuperar seu estado
-   Durável – esses TMs têm um log

Para criar um TM durável, você deve criar um log do CLFS e chamar [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ou fazer com que o KTM o crie para você. Depois que um TM durável é criado, você deve primeiro recuperar o TM chamando [**RecoverTransactionManager.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) Depois que o TM for recuperado, ele estará disponível para uso.

Se você recuperou um TM existente, todas as RMs associadas a esse TM começarão a receber mensagens de recuperação. Para obter mais informações, consulte [Processamento de recuperação](recovery-processing.md).

Em seguida, crie um gerenciador de recursos chamando [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) com o handle TM. O RM pode ser volátil ou durável. Somente as TMs duráveis podem ser usadas com RMs duráveis.

Ao trabalhar transaticamente, você se inslista na transação chamando [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)e especificando quais notificações receber.

**Observação**  Você pode começar a receber notificações antes que a chamada para [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) seja concluída.

Quando você receber uma notificação, chame a função "Complete" apropriada quando qualquer trabalho associado ao \* processamento da notificação for concluído. As funções completas são:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Se a qualquer momento um gerenciador de recursos não conseguir concluir o trabalho da transação ou se continuar renderizar seu aplicativo não conseguir desfazer o trabalho feito dentro da transação, você deverá reverter a transação chamando [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



