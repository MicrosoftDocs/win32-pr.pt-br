---
description: Quando um documento ou texto precisa ter privacidade protegida por um único usuário ou quando o documento é compartilhado entre um pequeno grupo de pessoas que têm acesso à mesma senha secreta, a criptografia/descriptografia simples pode ser feita.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Criptografando e descriptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922359"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="cdbe7-103">Criptografando e descriptografando dados</span><span class="sxs-lookup"><span data-stu-id="cdbe7-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="cdbe7-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cdbe7-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="cdbe7-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="cdbe7-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="cdbe7-107">Quando um documento ou texto precisa ter privacidade protegida por um único usuário ou quando o documento é compartilhado entre um pequeno grupo de pessoas que têm acesso à mesma senha secreta, a criptografia/descriptografia simples pode ser feita.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="cdbe7-108">O CAPICOM não oferece suporte ao \# tipo de conteúdo ENCRYPTEDDATA PKCS 7, mas usa uma estrutura ASN não padrão para EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="cdbe7-109">Portanto, somente o capicor pode descriptografar um objeto capicot EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="cdbe7-110">As seções a seguir mostram exemplos de criptografia e tarefas de descriptografia:</span><span class="sxs-lookup"><span data-stu-id="cdbe7-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="cdbe7-111">Criptografando uma mensagem no CAPICOM</span><span class="sxs-lookup"><span data-stu-id="cdbe7-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="cdbe7-112">Descriptografando uma mensagem no CAPICOM</span><span class="sxs-lookup"><span data-stu-id="cdbe7-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



