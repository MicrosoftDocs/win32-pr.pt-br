---
description: Há situações em que as chaves devem ser exportadas do ambiente seguro do CSP (provedor de serviços de criptografia) para o espaço de dados de um aplicativo. As chaves que foram exportadas são armazenadas em estruturas de BLOB de chaves criptografadas.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Armazenamento de chaves de criptografia e Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771813"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="db737-104">Armazenamento de chaves de criptografia e Exchange</span><span class="sxs-lookup"><span data-stu-id="db737-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="db737-105">Há situações em que as chaves devem ser exportadas do ambiente seguro do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para o espaço de dados de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db737-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="db737-106">As chaves que foram exportadas são armazenadas em estruturas de [*blob de chaves*](../secgloss/k-gly.md) criptografadas.</span><span class="sxs-lookup"><span data-stu-id="db737-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="db737-107">Há duas situações específicas em que é necessário exportar chaves:</span><span class="sxs-lookup"><span data-stu-id="db737-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="db737-108">Para salvar uma [*chave de sessão*](../secgloss/s-gly.md) para uso posterior por um aplicativo, se, por exemplo, um aplicativo tiver apenas criptografado um arquivo de banco de dados para ser descriptografado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="db737-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="db737-109">O aplicativo é responsável por armazenar a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="db737-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="db737-110">Isso é necessário porque os CSPs não preservam [*as chaves simétricas*](../secgloss/s-gly.md) da sessão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="db737-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="db737-111">Para enviar uma chave para outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="db737-111">To send a key to someone else.</span></span> <span data-ttu-id="db737-112">Isso seria mais fácil se os respectivos CSPs pudessem se comunicar diretamente, mas não conseguirem.</span><span class="sxs-lookup"><span data-stu-id="db737-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="db737-113">Como os CSPs não podem se comunicar, a chave deve ser exportada de um CSP, transmitida para o aplicativo de destino e, em seguida, importada para o CSP de destino.</span><span class="sxs-lookup"><span data-stu-id="db737-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="db737-114">Esse processo pode se tornar mais complicado se o caminho de comunicação não for confiável.</span><span class="sxs-lookup"><span data-stu-id="db737-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="db737-115">Em ambos os casos, um aplicativo deve armazenar uma chave de sessão fora do CSP por um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="db737-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="db737-116">Para obter mais informações, consulte [procedimento para armazenar uma chave de sessão](procedure-for-storing-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="db737-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
