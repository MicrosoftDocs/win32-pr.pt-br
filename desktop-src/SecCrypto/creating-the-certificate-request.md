---
description: O processo de criação de uma solicitação de certificado envolve a coleta de determinadas informações do solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Criando a solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755310"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="33608-103">Criando a solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="33608-103">Creating the Certificate Request</span></span>

<span data-ttu-id="33608-104">O processo de criação de uma solicitação de certificado envolve a coleta de determinadas informações do solicitante.</span><span class="sxs-lookup"><span data-stu-id="33608-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="33608-105">Normalmente, isso é feito por meio de algum tipo de interface do usuário (IU), embora as informações possam ser obtidas diretamente de um banco de dados sem a necessidade de uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="33608-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="33608-106">O nível de informações necessárias é definido pela política da autoridade de [*certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="33608-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="33608-107">Um exemplo das informações necessárias pode ser o seguinte:</span><span class="sxs-lookup"><span data-stu-id="33608-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="33608-108">Nome comum</span><span class="sxs-lookup"><span data-stu-id="33608-108">Common Name</span></span>
-   <span data-ttu-id="33608-109">Nome da unidade</span><span class="sxs-lookup"><span data-stu-id="33608-109">Unit Name</span></span>
-   <span data-ttu-id="33608-110">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="33608-110">Company Name</span></span>
-   <span data-ttu-id="33608-111">City</span><span class="sxs-lookup"><span data-stu-id="33608-111">City</span></span>
-   <span data-ttu-id="33608-112">Estado</span><span class="sxs-lookup"><span data-stu-id="33608-112">State</span></span>
-   <span data-ttu-id="33608-113">País/Região</span><span class="sxs-lookup"><span data-stu-id="33608-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="33608-114">A interface é projetada para fazer uma única solicitação para cada instância de Xenroll.</span><span class="sxs-lookup"><span data-stu-id="33608-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="33608-115">Uma instância de XEnroll separada deve ser criada para criar cada [*solicitação de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="33608-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="33608-116">Para obter informações sobre como usar o controle de registro de certificado para solicitar um certificado em linguagens de programação específicas, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="33608-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="33608-117">Exemplo de solicitação em C++</span><span class="sxs-lookup"><span data-stu-id="33608-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="33608-118">Exemplo de solicitação no VBScript</span><span class="sxs-lookup"><span data-stu-id="33608-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
