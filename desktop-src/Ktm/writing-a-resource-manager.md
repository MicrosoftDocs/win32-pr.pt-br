---
description: Se você estiver escrevendo um serviço ou componente e precisar usar serviços transacionais ou se precisar monitorar o estado de uma transação de kernel, você precisará criar um RM (Gerenciador de recursos).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escrevendo um Gerenciador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758456"
---
# <a name="writing-a-resource-manager"></a>Escrevendo um Gerenciador de recursos

Se você estiver escrevendo um serviço ou componente e precisar usar serviços transacionais ou se precisar monitorar o estado de uma transação de kernel, você precisará criar um RM (Gerenciador de recursos).

Para escrever um Gerenciador de recursos, você deve criar vários objetos kernel. Os objetos que um RM usa são:

-   Objetos do Gerenciador de transações (TM)
-   Objetos do Resource Manager
-   Objetos de inscrição

Primeiro, crie um objeto TM. Há dois tipos de TMs:

-   Volátil – esses TMs não têm um log e não podem recuperar seu estado
-   Durável – esses TMs têm um log

Para criar um TM durável, você deve criar um log do CLFS e chamar [**Createtransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ou fazer com que o KTM o crie para você. Depois que um TM durável é criado, você deve primeiro recuperar o TM chamando [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager). Depois que o TM for recuperado, ele estará disponível para uso.

Se você recuperou um TM existente, todo o RMs associado a este TM começará a receber mensagens de recuperação. Para obter mais informações, consulte [processamento de recuperação](recovery-processing.md).

Em seguida, você cria um Gerenciador de recursos chamando [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) com o identificador TM. O RM pode ser volátil ou durável. Somente TMs duráveis podem ser usados com RMs durável.

Ao trabalhar de forma transacional, você se inscreve na transação chamando [**Createalistaing**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)e especificando quais notificações receber.

**Observação**  Você pode começar a receber notificações antes que a chamada para [**createinscrita**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) seja concluída.

Quando você receber uma notificação, chame a função "concluída \* " apropriada quando qualquer trabalho associado ao processamento da notificação for concluído. As funções completas são:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Se, a qualquer momento, um Gerenciador de recursos não puder concluir o trabalho da transação, ou se continuar renderizando seu aplicativo para não conseguir desfazer o trabalho feito dentro da transação, você deverá reverter a transação chamando [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



