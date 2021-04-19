---
description: Controla a maneira como o WMI cria ou atualiza classes dependendo dos sinalizadores especificados.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
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
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796071"
---
# <a name="pragma-classflags"></a><span data-ttu-id="4aa91-103">pragma classflags</span><span class="sxs-lookup"><span data-stu-id="4aa91-103">pragma classflags</span></span>

<span data-ttu-id="4aa91-104">O comando **pragma classflags** pré-processador controla a maneira como o WMI cria ou atualiza classes dependendo dos sinalizadores especificados.</span><span class="sxs-lookup"><span data-stu-id="4aa91-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="4aa91-105">O seguinte descreve a sintaxe para este comando:</span><span class="sxs-lookup"><span data-stu-id="4aa91-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="4aa91-106">O *\[ sinalizador \]* deve ser um ou mais dos argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4aa91-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="4aa91-107">Você pode combinar qualquer sinalizador que não se contradizer.</span><span class="sxs-lookup"><span data-stu-id="4aa91-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="4aa91-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="4aa91-108">Flag</span></span>        | <span data-ttu-id="4aa91-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aa91-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa91-110">somente</span><span class="sxs-lookup"><span data-stu-id="4aa91-110">createonly</span></span>  | <span data-ttu-id="4aa91-111">Instrui o compilador a não fazer nenhuma alteração nas classes existentes e encerrar uma compilação se uma classe especificada no arquivo MOF já existir no WMI.</span><span class="sxs-lookup"><span data-stu-id="4aa91-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="4aa91-112">forceupdate</span><span class="sxs-lookup"><span data-stu-id="4aa91-112">forceupdate</span></span> | <span data-ttu-id="4aa91-113">Força atualizações de classes quando existem classes filhas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="4aa91-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="4aa91-114">Por exemplo, se você definir um qualificador de classe em uma classe filho e a classe base tentar adicionar o mesmo qualificador, o uso desse sinalizador fará com que o compilador resolva esse conflito excluindo o qualificador conflitante na classe filho.</span><span class="sxs-lookup"><span data-stu-id="4aa91-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="4aa91-115">Se a classe filho tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="4aa91-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="4aa91-116">safeupdate</span><span class="sxs-lookup"><span data-stu-id="4aa91-116">safeupdate</span></span>  | <span data-ttu-id="4aa91-117">Permite que o compilador atualize classes mesmo se houver classes filhas, se a alteração não causar conflitos com classes filhas.</span><span class="sxs-lookup"><span data-stu-id="4aa91-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="4aa91-118">Por exemplo, esse sinalizador permite que você adicione uma nova propriedade a uma classe base sem também precisar adicionar a propriedade a nenhuma classe filho pré-existente.</span><span class="sxs-lookup"><span data-stu-id="4aa91-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="4aa91-119">Se as classes filhas tiverem instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="4aa91-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="4aa91-120">updateonly</span><span class="sxs-lookup"><span data-stu-id="4aa91-120">updateonly</span></span>  | <span data-ttu-id="4aa91-121">Instrui o compilador a não criar novas classes e faz com que o compilador encerre a compilação se uma classe especificada no arquivo MOF não existir.</span><span class="sxs-lookup"><span data-stu-id="4aa91-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="4aa91-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4aa91-122">Examples</span></span>

<span data-ttu-id="4aa91-123">O exemplo a seguir mostra como usar esse comando com os sinalizadores UpdateOnly e forceupdate.</span><span class="sxs-lookup"><span data-stu-id="4aa91-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="4aa91-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aa91-124">Requirements</span></span>



| <span data-ttu-id="4aa91-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa91-125">Requirement</span></span> | <span data-ttu-id="4aa91-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4aa91-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4aa91-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aa91-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa91-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aa91-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4aa91-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aa91-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa91-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aa91-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4aa91-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4aa91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa91-132">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="4aa91-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




