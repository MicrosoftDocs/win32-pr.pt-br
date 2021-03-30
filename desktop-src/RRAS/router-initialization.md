---
title: Inicialização do roteador
description: As informações de configuração do roteador, os gerenciadores de roteadores e os protocolos/clientes de roteamento são divididos em informações globais e por informações de interface e são armazenados no registro e no arquivo de catálogo telefônico do roteador, router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- roteadores RRAS, inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634751"
---
# <a name="router-initialization"></a>Inicialização do roteador

As informações de configuração do roteador, os gerenciadores de roteadores e os protocolos/clientes de roteamento são divididos em informações globais e por informações de interface e são armazenados no registro e no arquivo de catálogo telefônico do roteador, router. pbk.

Quando o processo do roteador é iniciado, DIM (Dynamic interface Manager) lê a configuração do roteador no registro. DIM cria as interfaces que são especificadas pelas informações de interface.

DIM também recupera as informações globais do Gerenciador de roteador. DIM inicia os gerenciadores de roteador que correspondem a essas informações e transmite as informações. Por exemplo, se DIM encontrar informações globais para o Gerenciador de roteador IP no registro, DIM iniciará o Gerenciador de roteador IP e passará a ele as informações globais. Se nenhuma informação global estiver presente no registro para um Gerenciador de roteador específico, DIM não iniciará esse Gerenciador de roteador.

Os gerenciadores de roteadores examinam as informações globais recebidas do DIM. Se o Gerenciador de roteador encontrar informações específicas a um cliente específico dentro das informações globais, o Gerenciador de roteador carregará a DLL para o cliente (por exemplo IpNAT.dll) e inicializará o cliente chamando as funções [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) e [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) do cliente. O Gerenciador de roteador passa as informações globais específicas do cliente para o cliente na chamada para [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).

Em cada estágio, as informações passadas para a próxima entidade são opacas para a entidade que a precede. Ou seja, DIM não interpreta as informações globais para o Gerenciador do roteador IP, além do fato de que as informações são destinadas ao Gerenciador do roteador IP. Da mesma forma, o Gerenciador de roteador IP não interpreta as informações específicas do OSPF além do fato de que são informações de OSPF.

 

 




