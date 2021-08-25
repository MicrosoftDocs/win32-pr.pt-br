---
title: Namespaces de objeto kernel
description: Serviços de Área de Trabalho Remota usa vários namespaces para objetos kernel; um namespace global é usado principalmente por serviços em aplicativos cliente/servidor.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e1064638844039091dbe93aa1fedc75cb93f4aa1d012f8864e0154673c6cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989076"
---
# <a name="kernel-object-namespaces"></a>Namespaces de objeto kernel

Um servidor Serviços de Área de Trabalho Remota tem vários namespaces para os seguintes objetos kernel nomeados: eventos, semáforos, exclusões mútuas, temporizadores de espera, objetos de mapeamento de arquivo e objetos de trabalho. Há um namespace global usado principalmente por serviços em aplicativos cliente/servidor. além disso, cada sessão de cliente tem um namespace separado para esses objetos, como no Windows Vista.

Os namespaces de sessão de cliente separados permitem que vários clientes executem os mesmos aplicativos sem interferir uns com os outros. Para processos iniciados em uma sessão de cliente, o sistema usa o namespace de sessão por padrão. No entanto, esses processos podem usar o namespace global, \\ prefixando o prefixo "global" para o nome do objeto. Por exemplo, o código a seguir chama [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) e cria um objeto de evento chamado CSAPP no namespace global:

> [!Note]  
> o namespace global não está disponível para aplicativos da Windows Store.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Os aplicativos de serviço em um ambiente de Serviços de Área de Trabalho Remota usam o namespace global por padrão.

A sessão zero é usada somente para hospedar serviços e não há nenhuma sessão de console, diferente das versões anteriores do Windows.

O namespace global permite que processos em várias sessões de cliente se comuniquem com um aplicativo de serviço. Por exemplo, um aplicativo cliente/servidor pode usar um objeto mutex para sincronização. O módulo de servidor pode criar o objeto mutex no namespace global. Em seguida, uma sessão de cliente pode usar o prefixo "global \\ " para abrir o objeto mutex.

Outro uso do namespace global é para aplicativos que usam objetos nomeados para detectar que já existe uma instância do aplicativo em execução no sistema em todas as sessões. Esse objeto nomeado deve ser criado ou aberto no namespace global em vez do namespace por sessão. O caso mais comum de executar o aplicativo uma vez por sessão tem suporte por padrão, pois o objeto nomeado é criado em um namespace por sessão.

Além do prefixo "global \\ ", os processos de cliente podem usar o prefixo "local \\ " para criar explicitamente um objeto em seu namespace de sessão. Essas palavras-chave diferenciam maiúsculas de minúsculas.

O prefixo "session \\ " é reservado para uso do sistema e você não deve usá-lo em nomes de objetos kernel.

A troca rápida de usuário é implementada usando sessões Serviços de Área de Trabalho Remota. O primeiro usuário a fazer logon usa a sessão um, o próximo usuário a fazer logon usa a sessão dois e assim por diante. Os nomes de objeto de kernel devem seguir as diretrizes descritas para Serviços de Área de Trabalho Remota para que os aplicativos possam dar suporte a vários usuários.

A criação de um objeto de mapeamento de arquivo no namespace global, usando [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), de uma sessão diferente da sessão zero é uma operação privilegiada. Por isso, um aplicativo em execução em uma sessão de servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) arbitrária deve ter o [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) habilitado para criar um objeto de mapeamento de arquivo no namespace global com êxito. A verificação de privilégio é limitada à criação de objetos de mapeamento de arquivos e não se aplica à abertura de existentes. Por exemplo, se um serviço ou o sistema criar um objeto de mapeamento de arquivo, qualquer processo em execução em qualquer sessão poderá acessar esse objeto de mapeamento de arquivo, desde que o usuário tenha o acesso necessário.

 

 