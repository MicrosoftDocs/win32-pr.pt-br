---
description: Criptografia é o processo de conversão de dados de texto sem formatação (texto não criptografado) em algo que pareça aleatório e sem sentido (texto cifrado). A descriptografia é o processo de converter o texto cifrado de volta em texto não criptografado.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Criptografia e descriptografia de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090192"
---
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="e4bd8-104">Criptografia e descriptografia de dados</span><span class="sxs-lookup"><span data-stu-id="e4bd8-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="e4bd8-105">Criptografia é o processo de conversão de dados de texto sem formatação (texto não [*criptografado*](../secgloss/p-gly.md)) em algo que pareça aleatório e sem sentido ([*texto cifrado*](../secgloss/c-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="e4bd8-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="e4bd8-106">A descriptografia é o processo de converter o texto cifrado de volta em texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="e4bd8-107">Para criptografar mais de uma pequena quantidade de dados, a [*criptografia simétrica*](../secgloss/s-gly.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="e4bd8-108">Uma [*chave simétrica*](../secgloss/s-gly.md) é usada durante os processos de criptografia e descriptografia.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="e4bd8-109">Para descriptografar uma parte específica do texto cifrado, a chave que foi usada para criptografar os dados deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="e4bd8-110">A meta de cada algoritmo de criptografia é torná-lo o mais difícil possível de descriptografar o texto cifrado gerado sem usar a chave.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="e4bd8-111">Se um algoritmo de criptografia realmente bom for usado, não há nenhuma técnica significativamente melhor do que tentar cada chave de maneira metódica.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="e4bd8-112">Para esse algoritmo, quanto mais longa for a chave, mais difícil será descriptografar uma parte do texto cifrado sem possuir a chave.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="e4bd8-113">É difícil determinar a qualidade de um algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="e4bd8-114">Os algoritmos que parecem promissores, às vezes, são muito fáceis de quebrar, devido ao ataque adequado.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="e4bd8-115">Ao selecionar um algoritmo de criptografia, é uma boa ideia escolher um que tenha sido usado por vários anos e que tenha reparado com êxito todos os ataques.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="e4bd8-116">Para obter mais informações, consulte [funções de criptografia e](cryptography-functions.md)descriptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="e4bd8-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
