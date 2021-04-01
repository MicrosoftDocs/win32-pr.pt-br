---
description: A extensibilidade é obtida fornecendo-se o uso de novos identificadores de objeto (OIDs), novos tipos de codificação e novas DLLs.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Visão geral de OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829313"
---
# <a name="oid-overview"></a><span data-ttu-id="67cd6-103">Visão geral de OID</span><span class="sxs-lookup"><span data-stu-id="67cd6-103">OID Overview</span></span>

<span data-ttu-id="67cd6-104">A extensibilidade é obtida fornecendo-se o uso de novos [*identificadores de objeto*](../secgloss/o-gly.md) (OIDs), novos tipos de codificação e novas DLLs.</span><span class="sxs-lookup"><span data-stu-id="67cd6-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="67cd6-105">Os OIDs de CryptoAPI podem ter qualquer uma das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="67cd6-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="67cd6-106">Uma cadeia de caracteres numérica, como "1.2.3.500.88"</span><span class="sxs-lookup"><span data-stu-id="67cd6-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="67cd6-107">Uma cadeia de caracteres alfanumérica, como *MyFunction*</span><span class="sxs-lookup"><span data-stu-id="67cd6-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="67cd6-108">Uma constante com um valor menor ou igual a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="67cd6-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="67cd6-109">Essas constantes geralmente são associadas a um nome por meio do uso de uma instrução de **\# definição** em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="67cd6-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="67cd6-110">As funções extensíveis aceitam argumentos de tipo OID e Encoding.</span><span class="sxs-lookup"><span data-stu-id="67cd6-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="67cd6-111">Essas funções pesquisam o registro do sistema para localizar uma DLL associada aos argumentos de OID e tipo de codificação passados para a função.</span><span class="sxs-lookup"><span data-stu-id="67cd6-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="67cd6-112">Se uma DLL para a OID, a combinação de tipo de codificação for encontrada, a DLL será carregada e sua função será chamada.</span><span class="sxs-lookup"><span data-stu-id="67cd6-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="67cd6-113">A ilustração a seguir mostra esse fluxo para a função [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :</span><span class="sxs-lookup"><span data-stu-id="67cd6-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![fluxo de OID](images/oidflow.png)

<span data-ttu-id="67cd6-115">Isso permite que a funcionalidade da CryptoAPI seja estendida conforme a necessidade.</span><span class="sxs-lookup"><span data-stu-id="67cd6-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="67cd6-116">O uso dessa metodologia impõe um fardo no desenvolvedor da nova funcionalidade para gravar todo o código necessário para essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="67cd6-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="67cd6-117">Para codificar uma nova estrutura de dados, por exemplo, a função na DLL deve executar todo o processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="67cd6-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
