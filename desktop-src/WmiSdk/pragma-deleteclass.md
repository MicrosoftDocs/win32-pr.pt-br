---
description: Exclui uma classe existente e suas instâncias do repositório.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma DeleteClass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837175"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="27b5f-103">pragma DeleteClass</span><span class="sxs-lookup"><span data-stu-id="27b5f-103">pragma deleteclass</span></span>

<span data-ttu-id="27b5f-104">O comando **pragma DeleteClass** pré-processador exclui uma classe existente e suas instâncias do repositório.</span><span class="sxs-lookup"><span data-stu-id="27b5f-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="27b5f-105">O seguinte descreve a sintaxe:</span><span class="sxs-lookup"><span data-stu-id="27b5f-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="27b5f-106">*ClassName* é o nome da classe que o compilador do MOF exclui do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="27b5f-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="27b5f-107">O *\[ sinalizador \]* deve ser um dos argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="27b5f-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="27b5f-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="27b5f-108">Flag</span></span>   | <span data-ttu-id="27b5f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="27b5f-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b5f-110">falha</span><span class="sxs-lookup"><span data-stu-id="27b5f-110">fail</span></span>   | <span data-ttu-id="27b5f-111">Faz com que o compilador MOF saia com uma mensagem de erro se a classe ainda não existir no repositório.</span><span class="sxs-lookup"><span data-stu-id="27b5f-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="27b5f-112">nofail</span><span class="sxs-lookup"><span data-stu-id="27b5f-112">nofail</span></span> | <span data-ttu-id="27b5f-113">Faz com que o compilador MOF continue mesmo que a classe ainda não exista.</span><span class="sxs-lookup"><span data-stu-id="27b5f-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="27b5f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27b5f-114">Examples</span></span>

<span data-ttu-id="27b5f-115">O exemplo a seguir mostra como usar esse comando.</span><span class="sxs-lookup"><span data-stu-id="27b5f-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="27b5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27b5f-116">Requirements</span></span>



| <span data-ttu-id="27b5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="27b5f-117">Requirement</span></span> | <span data-ttu-id="27b5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="27b5f-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="27b5f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27b5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="27b5f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27b5f-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="27b5f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27b5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="27b5f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27b5f-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27b5f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="27b5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b5f-124">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="27b5f-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




