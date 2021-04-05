---
description: As informações neste tópico se aplicam ao Windows Server 2003 e ao Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocolo protocolo SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921615"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="65953-103">Protocolo protocolo SSL</span><span class="sxs-lookup"><span data-stu-id="65953-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="65953-104">As informações neste tópico se aplicam ao Windows Server 2003 e ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65953-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="65953-105">Para conjuntos de codificação para o Windows Server 2008 e o Windows Vista, consulte [pacotes de codificação no Schannel](cipher-suites-in-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="65953-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="65953-106">O Schannel dá suporte às versões 2,0 e 3,0 do [*protocolo protocolo SSL (SSL)*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="65953-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="65953-107">A partir do Windows 10, versão 1607 e Windows Server 2016, o SSL 2,0 foi removido e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="65953-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="65953-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="65953-108">SSL 3.0</span></span>

<span data-ttu-id="65953-109">O SSL 3,0 é o predecessor do [protocolo de segurança da camada de transporte](transport-layer-security-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="65953-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="65953-110">O Schannel dá suporte aos conjuntos de codificação listados em [TLS Cipher Suites](tls-cipher-suites.md) para SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="65953-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="65953-111">O SSL 3,0 dá suporte a todos os conjuntos de codificação listados em TLS Cipher Suites, bem como SSL \_ Fortezza \_ Kea \_ with \_ Fortezza \_ CBC \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="65953-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="65953-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="65953-112">SSL 2.0</span></span>

<span data-ttu-id="65953-113">O SSL 2,0 foi substituído pelo TLS e não deve ser usado para um novo desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="65953-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="65953-114">O Schannel dá suporte aos seguintes conjuntos de codificação para SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="65953-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="65953-115">Os pacotes são listados na ordem do mais seguro para o menos seguro.</span><span class="sxs-lookup"><span data-stu-id="65953-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="65953-116">SSL \_ RC4 \_ 128 \_ com \_ MD5</span><span class="sxs-lookup"><span data-stu-id="65953-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="65953-117">SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5</span><span class="sxs-lookup"><span data-stu-id="65953-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="65953-118">Protocolo \_ de criptografia RC2 \_ CBC \_ 128 \_ CBC \_ com \_ MD5</span><span class="sxs-lookup"><span data-stu-id="65953-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="65953-119">\_CBC SSL \_ des \_ 64 \_ com \_ MD5</span><span class="sxs-lookup"><span data-stu-id="65953-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="65953-120">SSL \_ RC4 \_ 128 \_ EXPORT40 \_ com \_ MD5</span><span class="sxs-lookup"><span data-stu-id="65953-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 
