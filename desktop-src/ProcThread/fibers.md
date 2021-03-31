---
description: Uma fibra é uma unidade de execução que deve ser agendada manualmente pelo aplicativo.
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: Fibras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0383e6d207a77c621f00f358c72bb8873ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662175"
---
# <a name="fibers"></a>Fibras

Uma *fibra* é uma unidade de execução que deve ser agendada manualmente pelo aplicativo. Os fibras são executados no contexto dos threads que os agendam. Cada thread pode agendar várias fibras. Em geral, os fibras não fornecem vantagens em relação a um aplicativo multithread bem projetado. No entanto, o uso de fibras pode facilitar a porta de aplicativos que foram projetados para agendar seus próprios threads.

Do ponto de vista do sistema, uma fibra assume a identidade do thread que a executa. Por exemplo, se um Fiber acessa o [armazenamento local de thread](thread-local-storage.md) (TLS), ele está acessando o armazenamento local de thread do thread que o está executando. Além disso, se uma fibra chamar a função [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) , o thread que a está executando será encerrado. No entanto, uma fibra não tem todas as mesmas informações de estado associadas a ela associadas a um thread. As informações de estado mantidas para uma fibra são sua pilha, um subconjunto de seus registros e os dados de fibra fornecidos durante a criação de fibra. Os registros salvos são o conjunto de registros normalmente preservados em uma chamada de função.

Fibras não são agendadas de preempção. Você agenda uma fibra alternando para ela de outra fibra. O sistema ainda agenda threads para execução. Quando um thread executando fibras é preempção, sua fibra atualmente em execução é preempção, mas permanece selecionada. A fibra selecionada é executada quando seu thread é executado.

Antes de agendar a primeira fibra, chame a função [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) para criar uma área na qual salvar informações de estado de fibra. O thread de chamada agora é a fibra em execução no momento. As informações de estado armazenadas para essa fibra incluem os dados de fibra passados como um argumento para **ConvertThreadToFiber**.

A função [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) é usada para criar uma nova fibra a partir de uma fibra existente; a chamada requer o tamanho da pilha, o endereço inicial e os dados de fibra. O endereço inicial normalmente é uma função fornecida pelo usuário, chamada função de fibra, que usa um parâmetro (os dados de fibra) e não retorna um valor. Se a função Fiber retornar, o thread que executa a fibra será encerrado. Para executar qualquer fibra criada com **CreateFiber**, chame a função [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) . Você pode chamar **SwitchToFiber** com o endereço de uma fibra criada por um thread diferente. Para fazer isso, você deve ter o endereço retornado para o outro thread quando ele chamou **CreateFiber** e você deve usar a sincronização adequada.

Uma fibra pode recuperar os dados de fibra chamando a macro [**GetFiberData**](/windows/win32/api/winnt/nf-winnt-getfiberdata) . Uma fibra pode recuperar o endereço de fibra a qualquer momento chamando a macro [**GetCurrentFiber**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber) .

## <a name="fiber-local-storage"></a>Armazenamento local de fibra

Uma fibra pode usar o *armazenamento local de fibra* (FLS) para criar uma cópia exclusiva de uma variável para cada fibra. Se não ocorrer nenhuma alternância de fibra, FLS agirá exatamente da mesma forma que o [armazenamento local de thread](thread-local-storage.md). As funções FLS ([**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc), [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree), [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)e [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)) manipulam os FLS associados ao thread atual. Se o thread estiver executando uma fibra e a fibra for trocada, o FLS também será alternado.

Para limpar os dados associados a uma fibra, chame a função [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) . Esses dados incluem a pilha, um subconjunto dos registros e os dados de fibra. Se a fibra atualmente em execução chamar **DeleteFiber**, seu thread chamará [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) e será encerrado. No entanto, se a fibra selecionada de um thread for excluída por uma fibra em execução em outro thread, o thread com a fibra excluída provavelmente será encerrado de forma anormal porque a pilha de fibra foi liberada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando fibras](using-fibers.md)
</dt> </dl>

 

 
