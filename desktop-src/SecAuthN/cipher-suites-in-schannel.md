---
description: Um pacote de criptografia é um pacote de algoritmos criptográficos.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Conjuntos de codificação em TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105748961"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a><span data-ttu-id="bddba-103">Conjuntos de codificação em TLS/SSL (Schannel SSP)</span><span class="sxs-lookup"><span data-stu-id="bddba-103">Cipher Suites in TLS/SSL (Schannel SSP)</span></span>

<span data-ttu-id="bddba-104">Um pacote de criptografia é um pacote de algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="bddba-104">A cipher suite is a set of cryptographic algorithms.</span></span> <span data-ttu-id="bddba-105">A implementação do SSP do Schannel dos protocolos TLS/SSL usam algoritmos de um conjunto de codificação para criar chaves e criptografar informações.</span><span class="sxs-lookup"><span data-stu-id="bddba-105">The schannel SSP implementation of the TLS/SSL protocols use algorithms from a cipher suite to create keys and encrypt information.</span></span> <span data-ttu-id="bddba-106">Um pacote de criptografia especifica um algoritmo para cada uma das seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="bddba-106">A cipher suite specifies one algorithm for each of the following tasks:</span></span>

-   <span data-ttu-id="bddba-107">Troca de chaves</span><span class="sxs-lookup"><span data-stu-id="bddba-107">Key exchange</span></span>
-   <span data-ttu-id="bddba-108">Criptografia em massa</span><span class="sxs-lookup"><span data-stu-id="bddba-108">Bulk encryption</span></span>
-   <span data-ttu-id="bddba-109">Autenticação de mensagem</span><span class="sxs-lookup"><span data-stu-id="bddba-109">Message authentication</span></span>

<span data-ttu-id="bddba-110">[*Algoritmos de troca de chaves*](/windows/desktop/SecGloss/k-gly) protegem as informações necessárias para criar chaves compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="bddba-110">[*Key exchange algorithms*](/windows/desktop/SecGloss/k-gly) protect information required to create shared keys.</span></span> <span data-ttu-id="bddba-111">Esses algoritmos são assimétricos ([*algoritmos de chave pública*](/windows/desktop/SecGloss/p-gly)) e têm um bom desempenho para quantidades relativamente pequenas de dados.</span><span class="sxs-lookup"><span data-stu-id="bddba-111">These algorithms are asymmetric ([*public key algorithms*](/windows/desktop/SecGloss/p-gly)) and perform well for relatively small amounts of data.</span></span>

<span data-ttu-id="bddba-112">Algoritmos de criptografia em massa criptografam mensagens trocadas entre clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="bddba-112">Bulk encryption algorithms encrypt messages exchanged between clients and servers.</span></span> <span data-ttu-id="bddba-113">Esses algoritmos são [*simétricos*](/windows/desktop/SecGloss/s-gly) e têm um bom desempenho para grandes quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="bddba-113">These algorithms are [*symmetric*](/windows/desktop/SecGloss/s-gly) and perform well for large amounts of data.</span></span>

<span data-ttu-id="bddba-114">Os algoritmos de [autenticação de mensagens](message-authentication-codes-in-schannel.md) geram [*hashes*](/windows/desktop/SecGloss/h-gly) de mensagens e assinaturas que garantem a [*integridade*](/windows/desktop/SecGloss/i-gly) de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bddba-114">[Message authentication](message-authentication-codes-in-schannel.md) algorithms generate message [*hashes*](/windows/desktop/SecGloss/h-gly) and signatures that ensure the [*integrity*](/windows/desktop/SecGloss/i-gly) of a message.</span></span>

<span data-ttu-id="bddba-115">Os desenvolvedores especificam esses elementos usando tipos de dados de [**\_ ID de alg**](/windows/desktop/SecCrypto/alg-id) .</span><span class="sxs-lookup"><span data-stu-id="bddba-115">Developers specify these elements by using [**ALG\_ID**](/windows/desktop/SecCrypto/alg-id) data types.</span></span> <span data-ttu-id="bddba-116">Para obter mais informações, consulte [especificando codificações Schannel e níveis de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="bddba-116">For more information, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="bddba-117">Nas versões anteriores do Windows, os conjuntos de criptografia TLS e as curvas elípticas foram configuradas usando uma única cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="bddba-117">In earlier versions of Windows, TLS cipher suites and elliptical curves were configured by using a single string:</span></span>

![Diagrama que mostra uma única cadeia de caracteres para um conjunto de codificação.](images/tls-cipher-suite.png)

<span data-ttu-id="bddba-119">Versões diferentes do Windows dão suporte a diferentes conjuntos de criptografia TLS e ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="bddba-119">Different Windows versions support different TLS cipher suites and priority order.</span></span> <span data-ttu-id="bddba-120">Consulte a versão correspondente do Windows para a ordem padrão na qual elas são escolhidas pelo provedor Microsoft Schannel.</span><span class="sxs-lookup"><span data-stu-id="bddba-120">See the corresponding Windows version for the default order in which they are chosen by the Microsoft Schannel Provider.</span></span>

<span data-ttu-id="bddba-121">**Windows Server 2022:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-121">**Windows Server 2022:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)</span></span>

<span data-ttu-id="bddba-122">**Windows 10, versão 1903:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-122">**Windows 10, version 1903:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)</span></span>

<span data-ttu-id="bddba-123">**Windows 10, versão 1809:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-123">**Windows 10, version 1809:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span></span>

<span data-ttu-id="bddba-124">**Windows 10, versão 1803:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-124">**Windows 10, version 1803:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span></span>

<span data-ttu-id="bddba-125">**Windows 10, versão 1709:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-125">**Windows 10, version 1709:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span></span>

<span data-ttu-id="bddba-126">**Windows 10, versão 1703:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-126">**Windows 10, version 1703:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span></span>

<span data-ttu-id="bddba-127">**Windows Server 2016 e Windows 10, versão 1607:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-127">**Windows Server 2016 and Windows 10, version 1607:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span></span>

<span data-ttu-id="bddba-128">**Windows 10, versão 1511:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-128">**Windows 10, version 1511:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)</span></span>

<span data-ttu-id="bddba-129">**Windows 10, versão 1507:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-129">**Windows 10, version 1507:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span></span>

<span data-ttu-id="bddba-130">**Windows Server 2012 R2 e Windows 8.1:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-130">**Windows Server 2012 R2 and Windows 8.1:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span></span>

<span data-ttu-id="bddba-131">**Windows Server 2012 e Windows 8:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 8](tls-cipher-suites-in-windows-8.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-131">**Windows Server 2012 and Windows 8:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8](tls-cipher-suites-in-windows-8.md)</span></span>

<span data-ttu-id="bddba-132">**Windows Server 2008 R2 e Windows 7:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 7](tls-cipher-suites-in-windows-7.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-132">**Windows Server 2008 R2 and Windows 7:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 7](tls-cipher-suites-in-windows-7.md)</span></span>

<span data-ttu-id="bddba-133">**Windows Server 2008 e Windows Vista:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows Vista](schannel-cipher-suites-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="bddba-133">**Windows Server 2008 and Windows Vista:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Vista](schannel-cipher-suites-in-windows-vista.md)</span></span>

<span data-ttu-id="bddba-134">**Windows Server 2003 e Windows XP:** Para obter informações sobre conjuntos de codificação com suporte, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bddba-134">**Windows Server 2003 and Windows XP:** For information about supported cipher suites, see the following topics.</span></span>

| <span data-ttu-id="bddba-135">Tópico</span><span class="sxs-lookup"><span data-stu-id="bddba-135">Topic</span></span>                                                                         | <span data-ttu-id="bddba-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="bddba-136">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bddba-137">Conjuntos de codificação TLS</span><span class="sxs-lookup"><span data-stu-id="bddba-137">TLS Cipher Suites</span></span>](tls-cipher-suites.md)<br/>                         | <span data-ttu-id="bddba-138">Informações sobre os conjuntos de codificação disponíveis com o protocolo TLS no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bddba-138">Information about the cipher suites available with the TLS protocol in Windows Server 2003 and Windows XP.</span></span><br/>              |
| [<span data-ttu-id="bddba-139">Protocolo protocolo SSL</span><span class="sxs-lookup"><span data-stu-id="bddba-139">Secure Sockets Layer Protocol</span></span>](secure-sockets-layer-protocol.md)<br/> | <span data-ttu-id="bddba-140">Informações gerais sobre SSL 2,0 e 3,0, incluindo os pacotes de codificação disponíveis no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bddba-140">General information about SSL 2.0 and 3.0, including the available cipher suites in Windows Server 2003 and Windows XP.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="bddba-141">Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva.</span><span class="sxs-lookup"><span data-stu-id="bddba-141">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="bddba-142">O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.</span><span class="sxs-lookup"><span data-stu-id="bddba-142">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>

 

