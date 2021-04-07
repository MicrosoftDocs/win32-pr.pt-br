---
description: Os gravadores de aplicativo podem fazer alterações de código-fonte secundárias para adicionar operações de registro e arquivo transacionado usando o KTM (kernel Transaction Manager).
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Trabalhando com transações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828716"
---
# <a name="working-with-transactions"></a>Trabalhando com transações

Os gravadores de aplicativo podem fazer alterações de código-fonte secundárias para adicionar operações de registro e arquivo transacionado usando o KTM (kernel Transaction Manager). Normalmente, isso envolverá a criação de uma transação e a passagem do identificador para outras funções fornecidas por recursos transacionais, como [NTFS Transacional](/windows/desktop/FileIO/transactional-ntfs-portal) e o registro transacionado.

O KTM fornece mecanismos para que seu aplicativo participe de transações, bem como para escrever seu próprio Gerenciador de recursos transacionais. Há funções que permitem criar, gerenciar e trabalhar com quatro classes de objetos kernel: transações, gerenciadores de transações, gerenciadores de recursos e inlistagens. Se você estiver simplesmente usando transações, só precisará trabalhar com objetos de transação e usar estas funções:

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Nunca presuma que uma transação está ativa. As transações podem ser revertidas por vários motivos e a qualquer momento.

O Windows expõe uma interface baseada em identificadores para recursos do sistema. Para trabalhar com um objeto do sistema operacional, o aplicativo primeiro solicita um identificador para o objeto e, em seguida, usa esse identificador em chamadas de função subsequentes para acessar ou modificar o objeto. Um identificador geralmente pode ser aberto em modos diferentes; o modo especificado afeta a semântica das chamadas de função subsequentes. Por exemplo, um identificador de arquivo que é aberto por uma chamada para [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) com o sinalizador *DwDesiredAccess* definido como **generic \_ Read** não pode ser usado em chamadas que modificam o arquivo.

Você pode coordenar com [Coordenador de transações distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) recursos de modo de usuário, como SQL ou MSMQ, e com recursos de modo kernel que usam o KTM. Primeiro, crie uma transação do DTC ou um objeto [**System. Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) e, em seguida, chame o objeto [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) , do qual você pode obter o identificador de KTM. O objeto **IKernelTransaction** cria uma transação de KTM que é subordinada à transação do DTC. Com esse identificador, você pode criar seus objetos transacionados, mas sinalizar o resultado da transação usando DTC ou **System. Transactions**.

 

 
