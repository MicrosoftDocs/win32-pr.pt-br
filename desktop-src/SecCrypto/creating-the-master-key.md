---
description: Uma chave mestra é o material de dados chave do qual outras chaves são derivadas.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Criando a chave mestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501551"
---
# <a name="creating-the-master-key"></a><span data-ttu-id="0a29f-103">Criando a chave mestra</span><span class="sxs-lookup"><span data-stu-id="0a29f-103">Creating the Master Key</span></span>

<span data-ttu-id="0a29f-104">Uma [*chave mestra*](../secgloss/m-gly.md) é o material de dados chave do qual outras chaves são derivadas.</span><span class="sxs-lookup"><span data-stu-id="0a29f-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="0a29f-105">Dependendo do protocolo e do conjunto de codificação usado, a chave mestra pode ter de 5 a 48 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="0a29f-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="0a29f-106">Para o CSP do [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) , a chave mestra é criada pelo lado do cliente e transferida para o servidor em um envelope RSA.</span><span class="sxs-lookup"><span data-stu-id="0a29f-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="0a29f-107">Para um CSP/Schannel [*Diffie-Hellman*](../secgloss/d-gly.md), a chave mestra é criada com a execução de um Diffie-Hellman troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="0a29f-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="0a29f-108">O código para criar e trocar chaves mestras é demonstrado em:</span><span class="sxs-lookup"><span data-stu-id="0a29f-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="0a29f-109">Código de cliente Diffie-Hellman para criar a chave mestra</span><span class="sxs-lookup"><span data-stu-id="0a29f-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="0a29f-110">Código de servidor Diffie-Hellman para criar a chave mestra</span><span class="sxs-lookup"><span data-stu-id="0a29f-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="0a29f-111">Código do cliente RSA para criar a chave mestra</span><span class="sxs-lookup"><span data-stu-id="0a29f-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="0a29f-112">Código do servidor RSA para criar a chave mestra</span><span class="sxs-lookup"><span data-stu-id="0a29f-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="0a29f-113">Especificando os algoritmos</span><span class="sxs-lookup"><span data-stu-id="0a29f-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 
