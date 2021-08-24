---
description: O número máximo de soquetes com suporte por um determinado provedor de serviços Windows Sockets é específico da implementação.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Número máximo de soquetes com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b567b9733dfb869c901ac499ca8dac66904c84bbe77d750780504acee076385f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569746"
---
# <a name="maximum-number-of-sockets-supported"></a>Número máximo de soquetes com suporte

O número máximo de soquetes com suporte por um determinado provedor de serviços Windows Sockets é específico da implementação. O provedor Microsoft Winsock limita o número máximo de soquetes com suporte apenas pela memória disponível no computador local. No entanto, provedores Winsock de terceiros podem ter limitações no número de soquetes com suporte. Um aplicativo não deve fazer suposições sobre a disponibilidade de um determinado número de soquetes. Para obter mais informações sobre este tópico, [**consulte WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ SET e select

Várias macros FD XXX são definidas no arquivo de título \_ *Winsock2.h* para uso na portação de aplicativos para Windows do ambiente UNIX. Essas macros são usadas com [**as funções select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) para portar aplicativos para Windows. O número máximo de soquetes que um aplicativo Windows Sockets pode usar não é afetado pela constante de manifesto FD \_ SETSIZE. Esse valor definido no *arquivo de título Winsock2.h* é usado na construção das estruturas [**FD \_ SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) usadas com **a função select.** O valor padrão em Winsock2.h é 64. Se um aplicativo for projetado para ser capaz de trabalhar com mais de 64 soquetes usando as funções **select** e **WSAPoll,** o implementador deverá definir o FD SETSIZE do manifesto em cada arquivo de origem antes de incluir o arquivo de título \_ *Winsock2.h.* Uma maneira de fazer isso pode ser incluir a definição dentro das opções do compilador no makefile. Por exemplo, você pode adicionar "-DFD SETSIZE=128" como uma opção à linha de comando \_ do compilador para Microsoft C++. É necessário enfatizar que a definição de FD SETSIZE como um valor específico não tem efeito sobre o número real de soquetes fornecidos por um provedor de serviços \_ Windows Sockets. Esse valor afeta apenas as macros FD \_ XXX usadas pelas funções **select** e **WSAPoll.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**FD \_ SET**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Selecione**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Considerações sobre programação winsock](winsock-programming-considerations.md)
</dt> <dt>

[**Wsastartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
