---
description: Os tipos de dados a seguir são usados por funções, interfaces e objetos de criptografia.
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: Tipos de dados de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748393"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="21df9-103">Tipos de dados de criptografia</span><span class="sxs-lookup"><span data-stu-id="21df9-103">Cryptography Data Types</span></span>

<span data-ttu-id="21df9-104">Os tipos de dados a seguir são usados por funções, interfaces e objetos de criptografia.</span><span class="sxs-lookup"><span data-stu-id="21df9-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="21df9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="21df9-105">Data type</span></span>                                                                      | <span data-ttu-id="21df9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="21df9-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21df9-107">**ID de ALG \_**</span><span class="sxs-lookup"><span data-stu-id="21df9-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="21df9-108">Especifica os identificadores de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="21df9-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="21df9-109">**\_resposta OCSP do servidor HCERT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21df9-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="21df9-110">Representa um identificador para uma resposta OCSP associada a uma cadeia de certificados de servidor.</span><span class="sxs-lookup"><span data-stu-id="21df9-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="21df9-111">**HCRYPTHASH**</span><span class="sxs-lookup"><span data-stu-id="21df9-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="21df9-112">Especifica identificadores para um [*objeto de hash*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="21df9-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="21df9-113">**HCRYPTKEY**</span><span class="sxs-lookup"><span data-stu-id="21df9-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="21df9-114">Especifica identificadores para chaves de criptografia.</span><span class="sxs-lookup"><span data-stu-id="21df9-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="21df9-115">**HCRYPTOIDFUNCADDR**</span><span class="sxs-lookup"><span data-stu-id="21df9-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="21df9-116">Representa um identificador para uma função que pode ser instalada usando um OID ( [*identificador de objeto*](../secgloss/o-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="21df9-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="21df9-117">**HCRYPTOIDFUNCSET**</span><span class="sxs-lookup"><span data-stu-id="21df9-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="21df9-118">Representa um identificador para um conjunto de funções que podem ser instaladas usando um OID.</span><span class="sxs-lookup"><span data-stu-id="21df9-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="21df9-119">**HCRYPTPROV \_ herdado**</span><span class="sxs-lookup"><span data-stu-id="21df9-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="21df9-120">Usado para substituir o tipo de dados [**HCRYPTPROV**](hcryptprov.md) em que o tipo de dados **HCRYPTPROV** não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="21df9-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="21df9-121">**\_identificador de chave HCRYPTPROV ou \_ NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21df9-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="21df9-122">Especifica um identificador para um [*provedor de serviços de criptografia*](../secgloss/c-gly.md) (CSP) ou CSP CNG do CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="21df9-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="21df9-123">**HCRYPTPROV**</span><span class="sxs-lookup"><span data-stu-id="21df9-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="21df9-124">Especifica um identificador para um CSP CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="21df9-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="21df9-125">**identificador de KEYSVCC \_**</span><span class="sxs-lookup"><span data-stu-id="21df9-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="21df9-126">Especifica identificadores para o serviço de chave.</span><span class="sxs-lookup"><span data-stu-id="21df9-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
