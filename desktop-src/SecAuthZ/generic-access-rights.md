---
description: Os objetos protegíveis usam um formato de máscara de acesso no qual os quatro bits de ordem superior especificam direitos de acesso genéricos.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Direitos de acesso genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662738"
---
# <a name="generic-access-rights"></a><span data-ttu-id="a09c6-103">Direitos de acesso genéricos</span><span class="sxs-lookup"><span data-stu-id="a09c6-103">Generic Access Rights</span></span>

<span data-ttu-id="a09c6-104">Os objetos protegíveis usam um [formato de máscara de acesso](access-mask-format.md) no qual os quatro bits de ordem superior especificam direitos de acesso genéricos.</span><span class="sxs-lookup"><span data-stu-id="a09c6-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="a09c6-105">Cada tipo de objeto protegível mapeia esses bits para um conjunto de seus direitos de acesso padrão e específicos de objeto.</span><span class="sxs-lookup"><span data-stu-id="a09c6-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="a09c6-106">Por exemplo, um objeto de arquivo do Windows mapeia o \_ bit de leitura genérico para o controle de leitura \_ e sincroniza os direitos de acesso padrão e os \_ direitos de \_ acesso específicos ao objeto ler dados, ler arquivo e \_ \_ \_ atributos de leitura de arquivo \_ .</span><span class="sxs-lookup"><span data-stu-id="a09c6-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="a09c6-107">Outros tipos de objetos mapeiam o \_ bit de leitura genérico para qualquer conjunto de direitos de acesso apropriado para esse tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="a09c6-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="a09c6-108">Você pode usar direitos de acesso genéricos para especificar o tipo de acesso que precisa ao abrir um identificador para um objeto.</span><span class="sxs-lookup"><span data-stu-id="a09c6-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="a09c6-109">Normalmente, isso é mais simples do que especificar todos os direitos padrão e específicos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a09c6-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="a09c6-110">A tabela a seguir mostra as constantes definidas para os direitos de acesso genéricos.</span><span class="sxs-lookup"><span data-stu-id="a09c6-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="a09c6-111">Constante</span><span class="sxs-lookup"><span data-stu-id="a09c6-111">Constant</span></span>         | <span data-ttu-id="a09c6-112">Significado genérico</span><span class="sxs-lookup"><span data-stu-id="a09c6-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="a09c6-113">\_tudo genérico</span><span class="sxs-lookup"><span data-stu-id="a09c6-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="a09c6-114">Todos os direitos de acesso possíveis</span><span class="sxs-lookup"><span data-stu-id="a09c6-114">All possible access rights</span></span> |
| <span data-ttu-id="a09c6-115">\_execução genérica</span><span class="sxs-lookup"><span data-stu-id="a09c6-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="a09c6-116">Acesso de execução</span><span class="sxs-lookup"><span data-stu-id="a09c6-116">Execute access</span></span>             |
| <span data-ttu-id="a09c6-117">\_leitura genérica</span><span class="sxs-lookup"><span data-stu-id="a09c6-117">GENERIC\_READ</span></span>    | <span data-ttu-id="a09c6-118">Acesso de leitura</span><span class="sxs-lookup"><span data-stu-id="a09c6-118">Read access</span></span>                |
| <span data-ttu-id="a09c6-119">\_gravação genérica</span><span class="sxs-lookup"><span data-stu-id="a09c6-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="a09c6-120">Acesso de gravação</span><span class="sxs-lookup"><span data-stu-id="a09c6-120">Write access</span></span>               |



 

<span data-ttu-id="a09c6-121">Os aplicativos que definem objetos protegíveis privados também podem usar os direitos de acesso genéricos.</span><span class="sxs-lookup"><span data-stu-id="a09c6-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



