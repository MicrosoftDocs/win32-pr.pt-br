---
description: Com as funções hash e assinatura digital, um usuário pode assinar digitalmente os dados para que qualquer outro usuário possa verificar se os dados não foram alterados desde que foram assinados. A identidade do usuário que assinou os dados também pode ser verificada.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes e assinaturas digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755046"
---
# <a name="hashes-and-digital-signatures"></a><span data-ttu-id="48731-104">Hashes e assinaturas digitais</span><span class="sxs-lookup"><span data-stu-id="48731-104">Hashes and Digital Signatures</span></span>

<span data-ttu-id="48731-105">Com as [funções hash e assinatura digital](cryptography-functions.md), um usuário pode assinar digitalmente os dados para que qualquer outro usuário possa verificar se os dados não foram alterados desde que foram assinados.</span><span class="sxs-lookup"><span data-stu-id="48731-105">With [Hash and Digital Signature Functions](cryptography-functions.md), a user can digitally sign data so that any other user can verify that the data has not been changed since it was signed.</span></span> <span data-ttu-id="48731-106">A identidade do usuário que assinou os dados também pode ser verificada.</span><span class="sxs-lookup"><span data-stu-id="48731-106">The identity of the user who signed the data can also be verified.</span></span>

<span data-ttu-id="48731-107">Uma [*assinatura digital*](../secgloss/d-gly.md) consiste em uma pequena quantidade de dados binários, normalmente menos de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="48731-107">A [*digital signature*](../secgloss/d-gly.md) consists of a small amount of binary data, typically less than 256 bytes.</span></span> <span data-ttu-id="48731-108">Essa assinatura pode ser agrupada com a mensagem assinada ou armazenada separadamente, dependendo de como um aplicativo específico foi implementado.</span><span class="sxs-lookup"><span data-stu-id="48731-108">This signature can be bundled with the signed message or stored separately, depending on how a particular application has been implemented.</span></span>

<span data-ttu-id="48731-109">O provedor de criptografia forte da Microsoft cria assinaturas digitais que estão em conformidade com os [*padrões de criptografia de chave pública*](../secgloss/p-gly.md) (PKCS) da RSA \# 1.</span><span class="sxs-lookup"><span data-stu-id="48731-109">The Microsoft Strong Cryptographic Provider creates digital signatures that conform to the RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1.</span></span>

 

 
