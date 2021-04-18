---
description: Todas as operações normais do RSA/Schannel e do Diffie-Hellman/Schannel usam o \_ par de chaves públicas/privadas do keyexchange.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Uso do par de chaves pública/privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800077"
---
# <a name="publicprivate-key-pair-usage"></a><span data-ttu-id="44351-103">Uso do par de chaves pública/privada</span><span class="sxs-lookup"><span data-stu-id="44351-103">Public/Private Key Pair Usage</span></span>

<span data-ttu-id="44351-104">Todas as operações normais do [*RSA*](../secgloss/r-gly.md)/Schannel e do [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel usam o \_ par de [*chaves públicas/privadas*](../secgloss/p-gly.md)do keyexchange.</span><span class="sxs-lookup"><span data-stu-id="44351-104">All normal [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel operations use the AT\_KEYEXCHANGE [*public/private key pair*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="44351-105">Para fornecer [*autenticação*](../secgloss/a-gly.md)de servidor, o lado do servidor de operações Schannel deve ter acesso ao seu certificado [*X. 509*](../secgloss/x-gly.md) contendo sua chave pública e acesso à [*chave privada*](../secgloss/p-gly.md)correspondente.</span><span class="sxs-lookup"><span data-stu-id="44351-105">To provide server [*authentication*](../secgloss/a-gly.md), the server-side of Schannel operations must have access to its [*X.509*](../secgloss/x-gly.md) certificate containing its public key and access to the matching [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="44351-106">O lado do cliente do [*Schannel*](../secgloss/s-gly.md) precisa de seu certificado com sua chave pública e acesso à sua chave privada se a autenticação do cliente for implementada.</span><span class="sxs-lookup"><span data-stu-id="44351-106">The client-side of [*Schannel*](../secgloss/s-gly.md) needs its certificate with its public key and access to its private key if client authentication is implemented.</span></span>

<span data-ttu-id="44351-107">Como os mecanismos de protocolo Schannel nunca usam o \_ par de chaves pública/privada da assinatura, esse par de chaves não precisa ter suporte de um novo CSP com suporte somente para RSA/Schannel ou Diffie-Hellman/Schannel.</span><span class="sxs-lookup"><span data-stu-id="44351-107">Since Schannel protocol engines never use the AT\_SIGNATURE public/private key pair, that key pair need not be supported by a new CSP supporting only RSA/Schannel or Diffie-Hellman/Schannel.</span></span>

<span data-ttu-id="44351-108">Se um mecanismo de protocolo usar um conjunto de codificação de exportação SSL 3,0 com um par de chaves AT- \_ Exchange com mais de 512 bits, o servidor deverá usar um par de chaves RSA adicional.</span><span class="sxs-lookup"><span data-stu-id="44351-108">If a protocol engine uses an SSL 3.0 export cipher suite with an AT\_KEYEXCHANGE key pair larger than 512 bits, the server must use an additional RSA key pair.</span></span> <span data-ttu-id="44351-109">Esse par de chaves adicional sempre é exatamente 512 bits e pode ser efêmero.</span><span class="sxs-lookup"><span data-stu-id="44351-109">This additional key pair is always exactly 512 bits and it can be ephemeral.</span></span> <span data-ttu-id="44351-110">O par é armazenado como um \_ elemento de keyexchange em um contêiner de chave de Propriedade do mecanismo de protocolo.</span><span class="sxs-lookup"><span data-stu-id="44351-110">The pair is stored as an AT\_KEYEXCHANGE element in a key container owned by the protocol engine.</span></span> <span data-ttu-id="44351-111">Um identificador para esse contêiner de chave normalmente é adquirido na inicialização do mecanismo de protocolo.</span><span class="sxs-lookup"><span data-stu-id="44351-111">A handle to this key container is typically acquired at protocol engine startup.</span></span>

<span data-ttu-id="44351-112">Diffie-Hellman dá suporte apenas a [*\_ \_ EPHEM DH CALG*](../secgloss/c-gly.md) e usa chaves públicas RSA ou DSS normais.</span><span class="sxs-lookup"><span data-stu-id="44351-112">Diffie-Hellman supports only [*CALG\_DH\_EPHEM*](../secgloss/c-gly.md) and uses normal RSA or DSS public keys.</span></span>

 

 
