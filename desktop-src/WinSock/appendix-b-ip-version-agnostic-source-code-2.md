---
description: Este apêndice ilustra uma versão reescrita dos aplicativos de exemplo Simplec. c e simples. c que tratam normalmente de um cliente habilitado para IPv4 ou IPv6. o código do servidor de CodeIPv6-Enabled de clientes habilitada para IPv6
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Apêndice B: código-fonte independente da versão IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827126"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>Apêndice B: código-fonte independente da versão IP

Este apêndice ilustra uma versão reescrita dos aplicativos de exemplo Simplec. c e simples. c que manipulam normalmente o IPv4 ou o IPv6.

-   [Código de cliente habilitado para IPv6](ipv6-enabled-client-code-2.md)
-   [Código de servidor habilitado para IPv6](ipv6-enabled-server-code-2.md)

Esse código exemplifica as diretrizes definidas neste guia IPv6 e está incluído para fornecer o código-fonte que foi modificado com êxito para adicionar suporte para IPv6. Este exemplo é intencionalmente simples, mas fornece um exemplo prático para o uso e a revisão. Uma versão somente IPv4 desse código-fonte é fornecida no [Apêndice A: código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md).

Ao comparar o código-fonte no apêndice A (somente IPv4) e no apêndice B (independente da versão IP), você tem uma noção das alterações necessárias para modificar o aplicativo Windows Sockets a fim de adicionar suporte para IPv6.

 

 



