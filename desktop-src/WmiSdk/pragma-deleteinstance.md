---
description: Exclui uma instância existente de uma classe do repositório.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010649"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="7931a-103">pragma deleteinstance</span><span class="sxs-lookup"><span data-stu-id="7931a-103">pragma deleteinstance</span></span>

<span data-ttu-id="7931a-104">O comando **pragma deleteinstance** exclui uma instância existente de uma classe do repositório.</span><span class="sxs-lookup"><span data-stu-id="7931a-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="7931a-105">O seguinte descreve a sintaxe para este comando:</span><span class="sxs-lookup"><span data-stu-id="7931a-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="7931a-106">*InstanceId* é um identificador exclusivo da instância que o compilador MOF exclui do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="7931a-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="7931a-107">O *\[ sinalizador \]* deve ser um dos argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7931a-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="7931a-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="7931a-108">Flag</span></span>   | <span data-ttu-id="7931a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7931a-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7931a-110">falha</span><span class="sxs-lookup"><span data-stu-id="7931a-110">fail</span></span>   | <span data-ttu-id="7931a-111">Faz com que o compilador MOF saia com uma mensagem de erro se a classe ainda não existir no repositório.</span><span class="sxs-lookup"><span data-stu-id="7931a-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="7931a-112">nofail</span><span class="sxs-lookup"><span data-stu-id="7931a-112">nofail</span></span> | <span data-ttu-id="7931a-113">Faz com que o compilador MOF continue mesmo que a classe ainda não exista.</span><span class="sxs-lookup"><span data-stu-id="7931a-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="7931a-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7931a-114">Examples</span></span>

<span data-ttu-id="7931a-115">O exemplo a seguir mostra como usar esse comando.</span><span class="sxs-lookup"><span data-stu-id="7931a-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="7931a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7931a-116">Requirements</span></span>



| <span data-ttu-id="7931a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7931a-117">Requirement</span></span> | <span data-ttu-id="7931a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7931a-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7931a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7931a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7931a-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7931a-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7931a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7931a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7931a-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7931a-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7931a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7931a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7931a-124">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="7931a-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




