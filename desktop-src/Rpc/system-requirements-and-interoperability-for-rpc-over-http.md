---
title: Requisitos de sistema RPC sobre HTTP, interoperabilidade
description: O Microsoft RPC dá suporte a RPC sobre HTTP, conforme mostrado na tabela a seguir.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104006960"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Requisitos de sistema RPC sobre HTTP, interoperabilidade

O Microsoft RPC dá suporte a RPC sobre HTTP, conforme mostrado na tabela a seguir.



| Plataforma                             | Suporta                       | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clientes, servidores e proxy RPC | Dá suporte a RPC sobre HTTP v1 e RPC sobre servidor e cliente HTTP v2. O proxy RPC dá suporte a RPC sobre HTTP v2 Quando o IIS está em execução no modo IIS 6,0. O proxy RPC dá suporte a RPC sobre HTTP v1 e RPC sobre HTTP v2 Quando o IIS está em execução no modo IIS 5,0. No entanto, a execução no modo do IIS 5,0 não é recomendada. Confira [recomendações de implantação de RPC sobre http](rpc-over-http-deployment-recommendations.md) para obter mais informações. O RPC sobre o servidor HTTP e o proxy RPC podem estar em computadores diferentes. |
| Windows XP com Service Pack 1 (SP1) | Clientes e servidores            | Dá suporte a RPC sobre HTTP v1 e RPC sobre servidor e cliente HTTP v2. Não oferece suporte a proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clientes e servidores            | Dá suporte somente a RPC por meio de cliente HTTP v1 e servidor. Não oferece suporte a proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clientes, servidores e proxy RPC | O RPC sobre o programa de servidor HTTP e o proxy RPC podem ser executados em computadores diferentes. RPC sobre o cliente HTTP, o servidor e o proxy RPC dão suporte somente a RPC sobre HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Além disso, os seguintes requisitos se aplicam:

-   O Windows 2000 e posterior requer o uso do IIS 4,0 ou posterior.
-   O RPC sobre proxy HTTP é executado somente nas edições do Windows Server.
-   Se o IIS estiver sendo executado em uma versão de servidor do Windows, o programa RPC sobre HTTP Server poderá ser executado em qualquer computador ao qual o proxy RPC esteja configurado para encaminhar o tráfego. Portanto, ele pode ser executado no mesmo computador que o proxy RPC ou em um computador diferente.

Para que uma conexão RPC sobre HTTP seja estabelecida, todo o RPC sobre o cliente HTTP, o servidor RPC sobre HTTP e o proxy RPC devem concordar em qual versão do RPC sobre HTTP é usada. Se não houver nenhuma versão comum do RPC sobre HTTP que todos os três suporte (cliente, servidor e proxy RPC), uma conexão RPC sobre HTTP não poderá ser estabelecida. A tabela a seguir resume essa interoperabilidade para versões diferentes do RPC sobre HTTP.



| RPC sobre cliente HTTP | Proxy RPC      | RPC sobre o servidor HTTP | Funcionamento?                                      | Versão usada     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| somente v1              | somente v1        | somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| somente v1              | somente v1        | V1 e v2       | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| somente v1              | V1 e v2 | somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| somente v1              | V1 e v2 | V1 e v2       | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| somente v1              | somente v2        | somente v1              | Não                                          |                  |
| somente v1              | somente v2        | V1 e v2       | Não                                          |                  |
| V1 e v2       | somente v1        | somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| V1 e v2       | somente v1        | V1 e v2       | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| V1 e v2       | V1 e v2 | somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| V1 e v2       | V1 e v2 | V1 e v2       | Sim                                         | RPC sobre HTTP v2 |
| V1 e v2       | somente v2        | somente v1              | Não                                          |                  |
| V1 e v2       | somente v2        | V1 e v2       | Sim. Essa é a configuração recomendada. | RPC sobre HTTP v2 |



 

Por exemplo, imagine um cliente do Windows 2000, um proxy do Windows Server 2003 com IIS em execução no modo IIS 6,0 e um servidor de RPC do Windows Server 2003 sobre HTTP. A primeira tabela nessa página de referência mostra que o Windows 2000 dá suporte apenas ao RPC sobre HTTP v1. A mesma tabela revela que um Windows Server 2003 com IIS em execução no modo IIS 6,0 dá suporte apenas ao RPC sobre HTTP V2 e que um servidor Windows Server 2003 RPC sobre HTTP é compatível com RPC sobre HTTP v1 e RPC sobre HTTP v2. Esse cenário é descrito na linha 6 da segunda tabela nessa página de referência, onde ele mostra que uma conexão RPC sobre HTTP não pode ser estabelecida. Além disso, a segunda tabela revela que existem duas opções para esse cenário:

-   Se a segurança e a robustez não forem uma consideração, o IIS poderá ser alternado para o modo do IIS 5,0, onde ele dá suporte a RPC sobre HTTP v1 e RPC sobre HTTP v2. Isso permitiria o estabelecimento de uma conexão RPC sobre HTTP v1.
-   Atualize o cliente do Windows 98 para o Windows XP com SP1 e obtenha a potência, a segurança e a robustez de uma conexão RPC sobre HTTP v2.

 

 




