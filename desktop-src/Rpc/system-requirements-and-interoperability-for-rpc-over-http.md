---
title: RPC sobre requisitos do sistema HTTP, interoperabilidade
description: O Microsoft RPC dá suporte a RPC em HTTP, conforme mostrado na tabela a seguir.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc9019789821499168a76d4d2e02ef485529e08b99c5f0759a19bfb4a46f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017306"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>RPC sobre requisitos do sistema HTTP, interoperabilidade

O Microsoft RPC dá suporte a RPC em HTTP, conforme mostrado na tabela a seguir.



| Plataforma                             | Suporta                       | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clientes, servidores e proxy RPC | Dá suporte a RPC por HTTP v1 e RPC por cliente e servidor HTTP v2. O Proxy RPC dá suporte a RPC em HTTP v2 quando o IIS está em execução no modo IIS 6.0. O Proxy RPC dá suporte a RPC por HTTP v1 e RPC por HTTP v2 quando o IIS está em execução no modo IIS 5.0. No entanto, a execução no modo IIS 5.0 não é recomendada. Consulte [RPC sobre a implantação de HTTP Recomendações](rpc-over-http-deployment-recommendations.md) para obter mais informações. O RPC sobre o servidor HTTP e o Proxy RPC podem estar em diferentes máquinas. |
| Windows XP com Service Pack 1 (SP1) | Clientes e servidores            | Dá suporte a RPC por HTTP v1 e RPC por cliente e servidor HTTP v2. Não dá suporte ao Proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clientes e servidores            | Dá suporte somente ao RPC por http v1 cliente e servidor. Não dá suporte ao Proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clientes, servidores e proxy RPC | O RPC sobre o programa de servidor HTTP e o Proxy RPC podem ser executados em computadores diferentes. O RPC sobre o cliente HTTP, o servidor e o Proxy RPC só são suportados por RPC por HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Além disso, os seguintes requisitos se aplicam:

-   Windows 2000 e posterior requer o uso do IIS 4.0 ou posterior.
-   O proxy RPC sobre HTTP é executado somente Windows edições de servidor.
-   Se o IIS estiver em execução em uma versão de servidor do Windows, o programa de servidor RPC via HTTP poderá ser executado em qualquer computador para o qual o Proxy RPC está configurado para encaminhar o tráfego. Portanto, ele pode ser executado no mesmo computador que o Proxy RPC ou em um computador diferente.

Para que uma conexão RPC sobre HTTP seja estabelecida, todo o RPC sobre o cliente HTTP, o RPC sobre o servidor HTTP e o Proxy RPC devem concordar com qual versão do RPC por HTTP é usada. Se não houver nenhuma versão comum do RPC por HTTP com suporte para todos os três (cliente, servidor e Proxy RPC), uma conexão RPC por HTTP não poderá ser estabelecida. A tabela a seguir resume essa interoperabilidade para diferentes versões do RPC por HTTP.



| RPC por cliente HTTP | RPC Proxy      | RPC sobre o servidor HTTP | Funciona?                                      | Versão usada     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| Somente v1              | Somente v1        | Somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| Somente v1              | Somente v1        | V1 e v2       | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| Somente v1              | V1 e v2 | Somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| Somente v1              | V1 e v2 | V1 e v2       | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| Somente v1              | Somente v2        | Somente v1              | Não                                          |                  |
| Somente v1              | Somente v2        | V1 e v2       | Não                                          |                  |
| V1 e v2       | Somente v1        | Somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| V1 e v2       | Somente v1        | V1 e v2       | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| V1 e v2       | V1 e v2 | Somente v1              | Sim, com limitações v1                    | RPC sobre HTTP v1 |
| V1 e v2       | V1 e v2 | V1 e v2       | Sim                                         | RPC sobre HTTP v2 |
| V1 e v2       | Somente v2        | Somente v1              | Não                                          |                  |
| V1 e v2       | Somente v2        | V1 e v2       | Sim. Essa é a configuração recomendada. | RPC sobre HTTP v2 |



 

Por exemplo, imagine um cliente Windows 2000, um proxy do Windows Server 2003 com o IIS em execução no modo IIS 6.0 e um RPC do Windows Server 2003 por servidor HTTP. A primeira tabela nesta página de referência mostra que Windows 2000 dá suporte apenas a RPC por HTTP v1. A mesma tabela revela que um Windows Server 2003 com o IIS em execução no modo IIS 6.0 dá suporte apenas a RPC por HTTP v2 e que um RPC do Windows Server 2003 por servidor HTTP dá suporte a RPC por HTTP v1 e RPC por HTTP v2. Esse cenário é descrito na linha 6 da segunda tabela nesta página de referência, em que mostra que não é possível estabelecer uma conexão RPC sobre HTTP. Além disso, a segunda tabela revela que existem duas opções para esse cenário:

-   Se a segurança e a robustez não são uma consideração, o IIS pode ser alternado para o modo IIS 5.0, em que dá suporte a RPC por HTTP v1 e RPC por HTTP v2. Isso habilitaria o estabelecimento de uma conexão RPC via HTTP v1.
-   Atualize o Windows 98 para o Windows XP com SP1 e obtenha a potência, a segurança e a robustez de uma conexão RPC sobre HTTP v2.

 

 




