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
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="1983c-103">Apêndice B: código-fonte independente da versão IP</span><span class="sxs-lookup"><span data-stu-id="1983c-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="1983c-104">Este apêndice ilustra uma versão reescrita dos aplicativos de exemplo Simplec. c e simples. c que manipulam normalmente o IPv4 ou o IPv6.</span><span class="sxs-lookup"><span data-stu-id="1983c-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="1983c-105">Código de cliente habilitado para IPv6</span><span class="sxs-lookup"><span data-stu-id="1983c-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="1983c-106">Código de servidor habilitado para IPv6</span><span class="sxs-lookup"><span data-stu-id="1983c-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="1983c-107">Esse código exemplifica as diretrizes definidas neste guia IPv6 e está incluído para fornecer o código-fonte que foi modificado com êxito para adicionar suporte para IPv6.</span><span class="sxs-lookup"><span data-stu-id="1983c-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="1983c-108">Este exemplo é intencionalmente simples, mas fornece um exemplo prático para o uso e a revisão.</span><span class="sxs-lookup"><span data-stu-id="1983c-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="1983c-109">Uma versão somente IPv4 desse código-fonte é fornecida no [Apêndice A: código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="1983c-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="1983c-110">Ao comparar o código-fonte no apêndice A (somente IPv4) e no apêndice B (independente da versão IP), você tem uma noção das alterações necessárias para modificar o aplicativo Windows Sockets a fim de adicionar suporte para IPv6.</span><span class="sxs-lookup"><span data-stu-id="1983c-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



