---
description: Os objetos nomeados fornecem uma maneira fácil para os processos compartilharem identificadores de objeto.
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: Nomes de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee746150a41f335a4073cb4b5ba282d17ad706f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749192"
---
# <a name="object-names"></a>Nomes de objeto

Os objetos nomeados fornecem uma maneira fácil para os processos compartilharem identificadores de objeto. Depois que um processo tiver criado um evento nomeado, mutex, semáforo ou objeto de timer, outros processos poderão usar o nome para chamar a função apropriada ( [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)ou [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)) para abrir um identificador para o objeto. A comparação de nomes diferencia maiúsculas de minúsculas.

Os nomes de evento, semáforo, mutex, timer de espera, mapeamento de arquivo e objetos de trabalho compartilham o mesmo namespace. Se você tentar criar um objeto usando um nome que está sendo usado por um objeto de outro tipo, a função falhará e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará **um \_ \_ identificador inválido de erro**. Portanto, ao criar objetos nomeados, use nomes exclusivos e certifique-se de verificar valores de retorno de função para erros de nome duplicado.

Se você tentar criar um objeto usando um nome que está sendo usado por um objeto do mesmo tipo, a função terá sucesso, retornando um identificador para o objeto existente e o erro de retorno de [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) **\_ já \_ existirá**. Por exemplo, se o nome especificado em uma chamada para a função [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) corresponder ao nome de um objeto mutex existente, a função retornará um identificador para o objeto existente. Nesse caso, a chamada para **CreateMutex** é equivalente a uma chamada para a função [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . Ter vários processos usam **CreateMutex** para o mesmo mutex é, portanto, equivalente a ter um processo que chama **CreateMutex** enquanto os outros processos chamam **OpenMutex**, exceto pelo fato de que ele elimina a necessidade de garantir que o processo de criação seja iniciado primeiro. No entanto, ao usar essa técnica para objetos mutex, nenhum dos processos de chamada deve solicitar a propriedade imediata do mutex. Se vários processos solicitarem a propriedade imediata, poderá ser difícil prever qual processo realmente Obtém a propriedade inicial.

Um ambiente de serviços de terminal tem um namespace global para eventos, semáforos, exclusões mútuas, temporizadores esperados, objetos de mapeamento de arquivos e objetos de trabalho. Além disso, cada sessão de cliente dos serviços de terminal tem seu próprio namespace separado para esses objetos. Os processos de cliente dos serviços de terminal podem usar nomes de objeto com um prefixo "global \\ " ou "local \\ " para criar explicitamente um objeto no namespace global ou de sessão. Para obter mais informações, consulte [namespaces de objeto kernel](../termserv/kernel-object-namespaces.md). A troca rápida de usuário é implementada usando sessões de serviços de terminal (cada usuário faz logon em uma sessão diferente). Os nomes de objeto de kernel devem seguir as diretrizes descritas para os serviços de terminal para que os aplicativos possam dar suporte a vários usuários.

Os objetos de sincronização podem ser criados em um namespace privado. Para obter mais informações, consulte [namespaces de objeto](object-namespaces.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando objetos nomeados](using-named-objects.md)
</dt> </dl>

 

 
