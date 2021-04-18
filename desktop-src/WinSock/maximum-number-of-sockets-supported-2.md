---
description: O número máximo de soquetes com suporte de um determinado provedor de serviços do Windows Sockets é específico da implementação.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Número máximo de soquetes com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768221"
---
# <a name="maximum-number-of-sockets-supported"></a>Número máximo de soquetes com suporte

O número máximo de soquetes com suporte de um determinado provedor de serviços do Windows Sockets é específico da implementação. O provedor Microsoft Winsock limita o número máximo de soquetes com suporte apenas pela memória disponível no computador local. No entanto, provedores de Winsock de terceiros podem ter limitações sobre os números de soquetes com suporte. Um aplicativo não deve fazer suposições sobre a disponibilidade de um determinado número de soquetes. Para obter mais informações sobre este tópico, consulte [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ set e Select

Várias \_ macros do FD xxx são definidas no arquivo de cabeçalho *Winsock2. h* para uso na portabilidade de aplicativos para o Windows a partir do ambiente UNIX. Essas macros são usadas com as funções [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) para portar aplicativos para o Windows. O número máximo de soquetes que um aplicativo do Windows Sockets pode usar não é afetado pela constante de manifesto FD \_ SetSize. Esse valor definido no arquivo de cabeçalho *Winsock2. h* é usado na construção das estruturas [**de \_ conjunto fd**](/windows/desktop/api/winsock/nf-winsock-fd_set) usadas com a função **Select** . O valor padrão em Winsock2. h é 64. Se um aplicativo for projetado para ser capaz de trabalhar com mais de 64 soquetes usando as funções **Select** e **WSAPoll** , o implementador deverá definir o manifesto FD \_ SetSize em todos os arquivos de origem antes de incluir o arquivo de cabeçalho *Winsock2. h* . Uma maneira de fazer isso pode ser incluir a definição nas opções do compilador no Makefile. Por exemplo, você pode adicionar "-DFD \_ SetSize = 128" como uma opção para a linha de comando do compilador para Microsoft C++. Deve-se enfatizar que definir FD \_ SetSize como um valor específico não tem nenhum efeito sobre o número real de soquetes fornecidos por um provedor de serviços do Windows Sockets. Esse valor afeta apenas as \_ macros do FD xxx usadas pelas funções **Select** e **WSAPoll** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**conjunto de FD \_**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Não**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
