---
description: Um hash de um texto ou outra cadeia de caracteres de bytes é um valor de comprimento fixo associado, estatisticamente exclusivo.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hashes de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837093"
---
# <a name="data-hashes"></a><span data-ttu-id="afd0c-103">Hashes de dados</span><span class="sxs-lookup"><span data-stu-id="afd0c-103">Data Hashes</span></span>

<span data-ttu-id="afd0c-104">Um [*hash*](../secgloss/h-gly.md) de um texto ou outra cadeia de caracteres de bytes é um valor de comprimento fixo associado, estatisticamente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="afd0c-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="afd0c-105">Em alguns documentos, um *hash* de um texto também é chamado de resumo; no entanto, nesta documentação o termo hash sempre será usado.</span><span class="sxs-lookup"><span data-stu-id="afd0c-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="afd0c-106">As funções de CryptoAPI fornecem um meio para criar um hash para qualquer texto ou outra cadeia de caracteres de bytes.</span><span class="sxs-lookup"><span data-stu-id="afd0c-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="afd0c-107">Esse hash, em seguida, pode ser usado como um identificador exclusivo de seus dados associados.</span><span class="sxs-lookup"><span data-stu-id="afd0c-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="afd0c-108">Para garantir a [*integridade*](../secgloss/i-gly.md) de um texto, um [*hash*](../secgloss/h-gly.md) de um texto pode ser enviado para acompanhar o texto.</span><span class="sxs-lookup"><span data-stu-id="afd0c-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="afd0c-109">O receptor pode então calcular um hash nos dados recebidos e comparar o hash calculado com o hash recebido.</span><span class="sxs-lookup"><span data-stu-id="afd0c-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="afd0c-110">Se as duas corresponderem, os dados recebidos deverão ser iguais aos dados dos quais o hash recebido foi criado.</span><span class="sxs-lookup"><span data-stu-id="afd0c-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="afd0c-111">Para obter um valor de hash, crie um objeto de hash usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="afd0c-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="afd0c-112">Esse objeto acumulará os dados a serem verificados.</span><span class="sxs-lookup"><span data-stu-id="afd0c-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="afd0c-113">Os dados são então adicionados ao objeto de hash com a função [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="afd0c-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="afd0c-114">Depois que o último bloco de dados é adicionado ao hash, a função [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) é usada para obter o valor de hash dos dados.</span><span class="sxs-lookup"><span data-stu-id="afd0c-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="afd0c-115">É fornecida mais segurança ao destruir o objeto de hash com [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) assim que o valor de hash tiver sido obtido.</span><span class="sxs-lookup"><span data-stu-id="afd0c-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
