---
description: Os códigos de erro a seguir são específicos para a API de instalação.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Códigos de erro (API de instalação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461263"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="7f1d1-103">Códigos de erro (API de instalação)</span><span class="sxs-lookup"><span data-stu-id="7f1d1-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="7f1d1-104">Os códigos de erro a seguir são específicos para a API de instalação.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="7f1d1-105">Erros de análise de INF</span><span class="sxs-lookup"><span data-stu-id="7f1d1-105">INF Parsing Errors</span></span>              | <span data-ttu-id="7f1d1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f1d1-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1d1-107">ERRO \_ esperado \_ nome da seção \_</span><span class="sxs-lookup"><span data-stu-id="7f1d1-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="7f1d1-108">Um nome de seção era esperado e não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="7f1d1-109">ERRO \_ de \_ \_ linha de nome de seção inadequada \_</span><span class="sxs-lookup"><span data-stu-id="7f1d1-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="7f1d1-110">O nome da seção não estava no formato correto.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-110">The section name was not of the correct format.</span></span> <span data-ttu-id="7f1d1-111">(Por exemplo, um nome não terminado por um colchete direito ( \] ).</span><span class="sxs-lookup"><span data-stu-id="7f1d1-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="7f1d1-112">nome da seção de erro \_ \_ \_ muito \_ longo</span><span class="sxs-lookup"><span data-stu-id="7f1d1-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="7f1d1-113">O nome da seção excedeu o comprimento máximo de Len de nome de separador máximo \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7f1d1-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="7f1d1-114">ERRO \_ de \_ sintaxe geral</span><span class="sxs-lookup"><span data-stu-id="7f1d1-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="7f1d1-115">A sintaxe geral está incorreta.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="7f1d1-116">Erros de tempo de execução INF</span><span class="sxs-lookup"><span data-stu-id="7f1d1-116">INF Runtime Errors</span></span>         | <span data-ttu-id="7f1d1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f1d1-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1d1-118">ERRO \_ de \_ estilo inf incorreto \_</span><span class="sxs-lookup"><span data-stu-id="7f1d1-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="7f1d1-119">O arquivo INF não é do tipo especificado na chamada de função.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="7f1d1-120">Por exemplo, esse erro pode ser retornado pela função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) se o arquivo inf foi desenvolvido para uma versão anterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="7f1d1-121">seção de erro \_ \_ não \_ encontrada</span><span class="sxs-lookup"><span data-stu-id="7f1d1-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="7f1d1-122">A seção não foi encontrada no arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="7f1d1-123">linha de erro \_ \_ não \_ encontrada</span><span class="sxs-lookup"><span data-stu-id="7f1d1-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="7f1d1-124">A linha não foi encontrada na seção INF.</span><span class="sxs-lookup"><span data-stu-id="7f1d1-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



