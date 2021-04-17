---
description: Embora esse mecanismo seja suficiente para aplicativos simples, ele não oferece suporte aos requisitos complexos de expedição de mensagens de aplicativos mais avançados, como aqueles que usam o modelo de interface de vários documentos (MDI).
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Gancho de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd098692784a662456c990a238bd309db0c321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771354"
---
# <a name="blocking-hook"></a>Gancho de bloqueio

Embora esse mecanismo seja suficiente para aplicativos simples, ele não oferece suporte aos requisitos complexos de expedição de mensagens de aplicativos mais avançados, como aqueles que usam o modelo de interface de vários documentos (MDI). Para tais aplicativos, um gancho de bloqueio específico de thread pode ser instalado pelo aplicativo. Isso será chamado pelo provedor de serviços, em vez do gancho de bloqueio padrão descrito no anterior. Um provedor de serviços deve recuperar um ponteiro para o gancho de bloqueio por thread do32.dll de ws2 \_ chamando [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback). Se o aplicativo não tiver instalado seu próprio gancho de bloqueio, um ponteiro para a função de gancho de bloqueio padrão será retornado.

Um provedor de serviços do Windows Sockets não pode supor que um gancho de bloqueio fornecido pelo aplicativo permite que o processamento de mensagens continue como o gancho de bloqueio padrão. Alguns aplicativos não podem tolerar a possibilidade de mensagens reentrante enquanto uma operação de bloqueio está pendente. Essa função de gancho de bloqueio de um aplicativo simplesmente retorna **false**. Se um provedor de serviços depender de mensagens para sua operação interna, ele poderá executar **PeekMessage**(hMyWnd...) antes de executar o gancho de bloqueio do aplicativo para que ele possa obter suas próprias mensagens sem afetar o restante do sistema.

Não há um gancho de bloqueio padrão instalado em versões multithreads preemptivas do Windows. Isso ocorre porque outros processos não serão bloqueados se um único aplicativo estiver aguardando a conclusão de uma operação (e, portanto, não chamar **PeekMessage** ou **GetMessage** , o que faz com que o aplicativo gere o processador em janelas não preventivas). Quando o provedor de serviços chama [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) , um ponteiro nulo será retornado indicando que o provedor deve usar funções de bloqueio do sistema operacional nativo. No entanto, para preservar a compatibilidade com versões anteriores, um gancho de bloqueio fornecido pelo aplicativo ainda pode ser instalado por thread no Windows.

O provedor de serviço Winsock chamará o gancho de bloqueio somente se todas as seguintes condições forem verdadeiras: a rotina é aquela que é definida como sendo capaz de bloquear, o soquete especificado é um soquete de bloqueio e a solicitação não pode ser concluída imediatamente. Se apenas soquetes de não bloqueio e [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) em vez de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) forem usados, o gancho de bloqueio nunca será chamado.

> [!Note]  
> Se, durante o tempo em que pseudoblocking estiver sendo usado para bloquear um thread, uma mensagem do Windows for recebida para o thread, haverá um risco de que o thread tente emitir outra chamada do Winsock. Devido à dificuldade de gerenciar essa condição com segurança, a especificação do Windows Sockets 1,1 não permitia esse comportamento. Não é permitido que um determinado thread faça várias chamadas de função Winsock aninhadas. Somente uma chamada de função pendente é permitida para um thread específico. Qualquer chamada de função Winsock aninhada falha com o erro WSAEINPROGRESS. Deve-se enfatizar que essa restrição se aplica a operações de bloqueio e não bloqueio, mas somente em ambientes do Windows Sockets 1,1. Há algumas exceções a essa regra, incluindo duas funções que permitem a um aplicativo determinar se uma operação pseudoblocking está na verdade em andamento e para cancelar essa operação, se necessário. Eles são descritos a seguir.

 

 

 
