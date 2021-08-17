---
description: Bloqueios de SRW (leitor/gravador) reduzidos permitem que os threads de um único processo acessem recursos compartilhados; Eles são otimizados para velocidade e ocupam muito pouca memória.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: Bloqueios de SRW (leitor/gravador) reduzidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc478d5f9bbfec1268f65b3e4a7f562b9bdca3d2df21f4570a52782eec9f028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959976"
---
# <a name="slim-readerwriter-srw-locks"></a>Bloqueios de SRW (leitor/gravador) reduzidos

Bloqueios de SRW (leitor/gravador) reduzidos permitem que os threads de um único processo acessem recursos compartilhados; Eles são otimizados para velocidade e ocupam muito pouca memória. Leitor reduzido-os bloqueios de gravador não podem ser compartilhados entre processos.

Os threads de leitor lêem dados de um recurso compartilhado, enquanto os threads do gravador gravam dados em um recurso compartilhado. Quando vários threads estão lendo e gravando usando um recurso compartilhado, bloqueios exclusivos, como uma seção crítica ou mutex, podem se tornar um afunilamento se os threads de leitor são executados continuamente, mas as operações de gravação são raras.

Os bloqueios de SRW fornecem dois modos nos quais os threads podem acessar um recurso compartilhado:

-   **Modo compartilhado**, que concede acesso somente leitura compartilhado a vários threads de leitor, o que permite que eles leiam dados do recurso compartilhado simultaneamente. Se operações de leitura excederem operações de gravação, essa simultaneidade aumentará o desempenho e a taxa de transferência em comparação com as seções críticas
    > [!NOTE]
    > Os bloqueios de SRW de modo compartilhado não devem ser adquiridos recursivamente, pois isso pode levar a deadlocks quando combinado com aquisição exclusiva.

-   **Modo exclusivo**, que concede acesso de leitura/gravação a um thread de gravador por vez. Quando o bloqueio for adquirido em modo exclusivo, nenhum outro thread poderá acessar o recurso compartilhado até que o gravador libere o bloqueio.
    > [!NOTE]
    > Os bloqueios de SRW em modo exclusivo não podem ser adquiridos recursivamente. Se um thread tentar adquirir um bloqueio que ele já contém, essa tentativa falhará (para [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) ou deadlock (para [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive))

Um único bloqueio de SRW pode ser adquirido em ambos os modos; os threads do leitor podem adquiri-lo no modo compartilhado, enquanto os threads do gravador podem adquiri-lo em modo exclusivo. Não há nenhuma garantia sobre a ordem em que os threads que solicitam a propriedade serão concedidos à propriedade; Os bloqueios de SRW não são justos nem FIFO.

Um bloqueio de SRW é o tamanho de um ponteiro. A vantagem é que é rápido atualizar o estado de bloqueio. A desvantagem é que muito poucas informações de estado podem ser armazenadas, portanto, os bloqueios de SRW não detectam o uso recursivo incorreto no modo compartilhado. Além disso, um thread que possui um bloqueio de SRW no modo compartilhado não pode atualizar sua propriedade do bloqueio para o modo exclusivo.

O chamador deve alocar uma estrutura SRWLOCK e inicializá-la chamando [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (para inicializar a estrutura dinamicamente) ou atribuir a constante **SRWLock \_ init** à variável de estrutura (para inicializar a estrutura estaticamente).

Você pode usar [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) para localizar o uso recursivo (reentrante) de bloqueios de SRW.

A seguir estão as funções de bloqueio de SRW.

| Função de bloqueio de SRW                                                | Descrição                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Adquire um bloqueio de SRW em modo exclusivo.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Adquire um bloqueio de SRW no modo compartilhado.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Inicializar um bloqueio de SRW.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Libera um bloqueio de SRW que foi aberto em modo exclusivo.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Libera um bloqueio de SRW que foi aberto no modo compartilhado.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Dorme na variável de condição especificada e libera o bloqueio especificado como uma operação atômica.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Tenta adquirir um bloqueio de SRW (leitor/gravador) reduzido no modo exclusivo. Se a chamada for bem-sucedida, o thread de chamada assumirá a propriedade do bloqueio. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Tenta adquirir um bloqueio de SRW (leitor/gravador) reduzido no modo compartilhado. Se a chamada for bem-sucedida, o thread de chamada assumirá a propriedade do bloqueio.    |

 
