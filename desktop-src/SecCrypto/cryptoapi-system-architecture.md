---
description: Explica a arquitetura do sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Arquitetura do sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296277"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="2bbd0-103">Arquitetura do sistema CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="2bbd0-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="2bbd0-104">A arquitetura do sistema CryptoAPI é composta de cinco áreas funcionais principais:</span><span class="sxs-lookup"><span data-stu-id="2bbd0-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="2bbd0-105">Funções de criptografia base</span><span class="sxs-lookup"><span data-stu-id="2bbd0-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="2bbd0-106">Funções de codificação/decodificação de certificado</span><span class="sxs-lookup"><span data-stu-id="2bbd0-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="2bbd0-107">Funções de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="2bbd0-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="2bbd0-108">Funções de mensagens simplificadas</span><span class="sxs-lookup"><span data-stu-id="2bbd0-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="2bbd0-109">Funções de mensagem de nível baixo</span><span class="sxs-lookup"><span data-stu-id="2bbd0-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="2bbd0-110">Funções de criptografia base</span><span class="sxs-lookup"><span data-stu-id="2bbd0-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="2bbd0-111">*Funções de contexto* usadas para se conectar a um CSP.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="2bbd0-112">Essas funções permitem que os aplicativos escolham um CSP específico por nome ou escolham um CSP específico que possa fornecer uma classe necessária de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="2bbd0-113">[*Funções de geração de chave*](../secgloss/k-gly.md) usadas para gerar e armazenar [*chaves criptográficas*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2bbd0-114">O suporte completo está incluído para alterar os [*modos de encadeamento*](../secgloss/c-gly.md), os [*vetores de inicialização*](../secgloss/i-gly.md)e outros recursos de criptografia.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="2bbd0-115">Para obter mais informações, consulte [funções de geração de chave e troca](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="2bbd0-116">*Funções de troca de chaves* usadas para trocar ou transmitir chaves.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="2bbd0-117">Para obter mais informações, consulte [armazenamento de chaves de criptografia e troca](cryptographic-key-storage-and-exchange.md) e [funções de geração de chave e do Exchange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="2bbd0-118">Funções de codificação/decodificação de certificado</span><span class="sxs-lookup"><span data-stu-id="2bbd0-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="2bbd0-119">Funções usadas para criptografar ou descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="2bbd0-120">O suporte também está incluído para dados de [*hash*](../secgloss/h-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2bbd0-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="2bbd0-121">Para obter mais informações, consulte [funções de criptografia de dados e](cryptography-functions.md) descriptografia e [criptografia e descriptografia de dados](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="2bbd0-122">Funções de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="2bbd0-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="2bbd0-123">Funções usadas para gerenciar coleções de certificados digitais.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="2bbd0-124">Para obter mais informações, consulte [certificados digitais](digital-certificates.md) e [funções de repositório de certificados](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="2bbd0-125">Funções de mensagens simplificadas</span><span class="sxs-lookup"><span data-stu-id="2bbd0-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="2bbd0-126">Funções usadas para criptografar e descriptografar mensagens e dados.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="2bbd0-127">Funções usadas para assinar mensagens e dados.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="2bbd0-128">Funções usadas para verificar a autenticidade de assinaturas em mensagens recebidas e dados relacionados.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="2bbd0-129">Para obter mais informações, consulte [mensagens simplificadas](simplified-messages.md) e [funções de mensagens simplificadas](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="2bbd0-130">Funções de mensagem de nível baixo</span><span class="sxs-lookup"><span data-stu-id="2bbd0-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="2bbd0-131">Funções usadas para executar todas as tarefas executadas pelas funções de mensagem simplificadas.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="2bbd0-132">As funções de mensagem de nível baixo fornecem mais flexibilidade do que as funções de mensagem simplificadas, mas exigem mais chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="2bbd0-133">Para obter mais informações, consulte [mensagens de nível inferior](low-level-messages.md) e [funções de mensagens de nível baixo](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![arquitetura de CryptoAPI](images/cryparch.png)

<span data-ttu-id="2bbd0-135">Cada uma das áreas funcionais tem uma palavra-chave em seu nome de função que indica sua área funcional.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="2bbd0-136">Área funcional</span><span class="sxs-lookup"><span data-stu-id="2bbd0-136">Functional area</span></span>              | <span data-ttu-id="2bbd0-137">Convenção de nome de função</span><span class="sxs-lookup"><span data-stu-id="2bbd0-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="2bbd0-138">Funções de criptografia base</span><span class="sxs-lookup"><span data-stu-id="2bbd0-138">Base cryptographic functions</span></span> | <span data-ttu-id="2bbd0-139">Confuso</span><span class="sxs-lookup"><span data-stu-id="2bbd0-139">Crypt</span></span>                    |
| <span data-ttu-id="2bbd0-140">Funções de codificação/decodificação</span><span class="sxs-lookup"><span data-stu-id="2bbd0-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="2bbd0-141">Confuso</span><span class="sxs-lookup"><span data-stu-id="2bbd0-141">Crypt</span></span>                    |
| <span data-ttu-id="2bbd0-142">Funções de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="2bbd0-142">Certificate store functions</span></span>  | <span data-ttu-id="2bbd0-143">Repositório</span><span class="sxs-lookup"><span data-stu-id="2bbd0-143">Store</span></span>                    |
| <span data-ttu-id="2bbd0-144">Funções de mensagens simplificadas</span><span class="sxs-lookup"><span data-stu-id="2bbd0-144">Simplified message functions</span></span> | <span data-ttu-id="2bbd0-145">Mensagem</span><span class="sxs-lookup"><span data-stu-id="2bbd0-145">Message</span></span>                  |
| <span data-ttu-id="2bbd0-146">Funções de mensagem de nível baixo</span><span class="sxs-lookup"><span data-stu-id="2bbd0-146">Low-level message functions</span></span>  | <span data-ttu-id="2bbd0-147">MSG</span><span class="sxs-lookup"><span data-stu-id="2bbd0-147">Msg</span></span>                      |



 

<span data-ttu-id="2bbd0-148">Os aplicativos usam funções em todas essas áreas.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="2bbd0-149">Essas funções, juntas, compõem o CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="2bbd0-150">As [*funções de criptografia base*](../secgloss/b-gly.md) usam os CSPs para os algoritmos de criptografia necessários e para a geração e o armazenamento seguro de [chaves de criptografia](cryptographic-keys.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="2bbd0-151">Dois tipos diferentes de chaves de criptografia são usados: [*chaves de sessão*](../secgloss/s-gly.md), que são usadas para criptografia/descriptografia única e [*pares de chaves pública/privada*](../secgloss/p-gly.md), que são usadas de forma mais permanente.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="2bbd0-152">Embora um aplicativo possa se comunicar diretamente com qualquer uma das cinco áreas funcionais, ele não pode se comunicar diretamente com um CSP.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="2bbd0-153">Todas as comunicações de aplicativo para CSP ocorrem por meio das [*funções criptográficas base*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd0-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="2bbd0-154">As funções criptográficas base têm um parâmetro que especifica qual CSP usar.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="2bbd0-155">Esse parâmetro pode ser definido como **nulo** para selecionar um CSP padrão.</span><span class="sxs-lookup"><span data-stu-id="2bbd0-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
