---
description: Controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171802"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="06e8e-103">pragma instanceflags</span><span class="sxs-lookup"><span data-stu-id="06e8e-103">pragma instanceflags</span></span>

<span data-ttu-id="06e8e-104">O comando **pragma instanceflags** pré-processador controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.</span><span class="sxs-lookup"><span data-stu-id="06e8e-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="06e8e-105">O seguinte descreve a sintaxe:</span><span class="sxs-lookup"><span data-stu-id="06e8e-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="06e8e-106">O *\[ sinalizador \]* deve ser um dos argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="06e8e-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="06e8e-107">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="06e8e-107">Flag</span></span>       | <span data-ttu-id="06e8e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="06e8e-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e8e-109">somente</span><span class="sxs-lookup"><span data-stu-id="06e8e-109">createonly</span></span> | <span data-ttu-id="06e8e-110">Impede que o compilador altere quaisquer instâncias existentes no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="06e8e-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="06e8e-111">updateonly</span><span class="sxs-lookup"><span data-stu-id="06e8e-111">updateonly</span></span> | <span data-ttu-id="06e8e-112">Impede que o compilador crie novas instâncias se uma instância especificada no arquivo MOF não existir.</span><span class="sxs-lookup"><span data-stu-id="06e8e-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="06e8e-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06e8e-113">Examples</span></span>

<span data-ttu-id="06e8e-114">O exemplo a seguir mostra como usar esse comando.</span><span class="sxs-lookup"><span data-stu-id="06e8e-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="06e8e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06e8e-115">Requirements</span></span>



| <span data-ttu-id="06e8e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e8e-116">Requirement</span></span> | <span data-ttu-id="06e8e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="06e8e-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="06e8e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06e8e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06e8e-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06e8e-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="06e8e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06e8e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06e8e-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06e8e-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06e8e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="06e8e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e8e-123">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="06e8e-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




