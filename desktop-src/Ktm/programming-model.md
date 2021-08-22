---
description: Os autores de aplicativos podem fazer pequenas alterações no código-fonte para adicionar operações transaciondas de arquivo e registro usando o KTM (Kernel Transaction Manager).
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Trabalhando com transações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda967e3c8fe165c3a59de6534c26bc125dfb8dd209be68b5914ea099b0023e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146509"
---
# <a name="working-with-transactions"></a>Trabalhando com transações

Os autores de aplicativos podem fazer pequenas alterações no código-fonte para adicionar operações transaciondas de arquivo e registro usando o KTM (Kernel Transaction Manager). Normalmente, isso envolverá a criação de uma transação e a passagem do handle para outras funções fornecidas por recursos transacionais, como [O NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) Transacional e o Registro Transacionado.

O KTM fornece mecanismos para seu aplicativo participar de transações, bem como escrever seu próprio gerenciador de recursos transacional. Há funções que permitem criar, gerenciar e trabalhar com quatro classes de objetos de kernel: transações, gerenciadores de transações, gerenciadores de recursos e inscrições. Se você estiver simplesmente usando transações, só precisará trabalhar com objetos de transação e usar estas funções:

-   [**Createtransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**Committransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Nunca suponha que uma transação está ativa. As transações podem ser re roleadas por vários motivos e a qualquer momento.

Windows expõe uma interface baseada em alça para recursos do sistema. Para trabalhar com um objeto do sistema operacional, o aplicativo primeiro solicita um identificador para o objeto e, em seguida, usa esse identificador em chamadas de função subsequentes para acessar ou modificar o objeto. Um handle geralmente pode ser aberto em modos diferentes; o modo especificado afeta a semântica de chamadas de função subsequentes. Por exemplo, um alça de arquivo aberto por uma chamada para [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) com o sinalizador *dwDesiredAccess* definido como **GENERIC \_ READ** não pode ser usado em chamadas que modificam o arquivo.

Você pode coordenar com [Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) de modo de usuário, como SQL ou MSMQ, e com recursos de modo kernel que usam o KTM. Primeiro, crie uma transação DTC ou um objeto [**System.Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) e, em seguida, chame o objeto [**IKernelTransaction,**](/previous-versions/windows/desktop/aa344210(v=vs.85)) do qual você pode obter o identificador KTM. O **objeto IKernelTransaction** cria uma transação KTM subordinada à transação DTC. Com esse alçamento, você pode criar seus objetos transacionados, mas sinalizar o resultado da transação usando DTC ou **System.Transactions.**

 

 
