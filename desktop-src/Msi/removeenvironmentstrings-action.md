---
description: A ação RemoveEnvironmentStrings modifica os valores das variáveis de ambiente.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Ação RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792488"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="70d92-103">Ação RemoveEnvironmentStrings</span><span class="sxs-lookup"><span data-stu-id="70d92-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="70d92-104">A ação RemoveEnvironmentStrings modifica os valores das variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="70d92-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="70d92-105">Observe que as variáveis de ambiente não são alteradas para a instalação em andamento quando a ação [WriteEnvironmentStrings](writeenvironmentstrings-action.md) ou a ação RemoveEnvironmentStrings são executadas.</span><span class="sxs-lookup"><span data-stu-id="70d92-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="70d92-106">No Windows 2000, essas informações são armazenadas no registro e uma mensagem é enviada para notificar o sistema sobre as alterações quando a instalação for concluída.</span><span class="sxs-lookup"><span data-stu-id="70d92-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="70d92-107">Um novo processo ou outro processo que verifica essas mensagens usará as novas variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="70d92-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="70d92-108">O instalador executa a [ação WriteEnvironmentStrings](writeenvironmentstrings-action.md) somente durante a instalação ou reinstalação de um componente e executa a ação RemoveEnvironmentStrings somente durante a remoção de um componente.</span><span class="sxs-lookup"><span data-stu-id="70d92-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="70d92-109">Os valores são gravados ou removidos com base na seleção de ações e modificadores primários.</span><span class="sxs-lookup"><span data-stu-id="70d92-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="70d92-110">Eles são descritos na seção mensagens ActionData a seguir.</span><span class="sxs-lookup"><span data-stu-id="70d92-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="70d92-111">Observe que, dependendo da ação especificada, WriteEnvironmentStrings pode remover variáveis e RemoveEnvironmentStrings pode adicioná-las com base na criação da [tabela de ambiente](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="70d92-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="70d92-112">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="70d92-112">Sequence Restrictions</span></span>

<span data-ttu-id="70d92-113">A [ação InstallValidate](installvalidate-action.md) deve ser executada antes da ação RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="70d92-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="70d92-114">Como a ação WriteEnvironmentStrings e a ação RemoveEnvironmentStrings nunca são aplicadas durante a instalação ou remoção de um componente, sua sequência relativa não é restrita.</span><span class="sxs-lookup"><span data-stu-id="70d92-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="70d92-115">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="70d92-115">ActionData Messages</span></span>



| <span data-ttu-id="70d92-116">Campo</span><span class="sxs-lookup"><span data-stu-id="70d92-116">Field</span></span> | <span data-ttu-id="70d92-117">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="70d92-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d92-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="70d92-118">\[1\]</span></span> | <span data-ttu-id="70d92-119">Nome da variável de ambiente a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="70d92-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="70d92-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="70d92-120">\[2\]</span></span> | <span data-ttu-id="70d92-121">O valor da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="70d92-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="70d92-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="70d92-122">\[3\]</span></span> | <span data-ttu-id="70d92-123">Esse é um campo de sinalizadores de bit que especificam a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="70d92-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="70d92-124">Inclua apenas um bit para uma ação principal.</span><span class="sxs-lookup"><span data-stu-id="70d92-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="70d92-125">Pode haver mais de um bit modificador incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="70d92-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="70d92-126">Consulte as seguintes descrições de sinalizador de bits.</span><span class="sxs-lookup"><span data-stu-id="70d92-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="70d92-127">Valor de bit</span><span class="sxs-lookup"><span data-stu-id="70d92-127">Bit value</span></span> | <span data-ttu-id="70d92-128">Descrição das ações principais</span><span class="sxs-lookup"><span data-stu-id="70d92-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d92-129">0x1</span><span class="sxs-lookup"><span data-stu-id="70d92-129">0x1</span></span>       | <span data-ttu-id="70d92-130">Definido.</span><span class="sxs-lookup"><span data-stu-id="70d92-130">Set.</span></span> <span data-ttu-id="70d92-131">Define o valor da variável de ambiente em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="70d92-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="70d92-132">Se esse bit for combinado com um bit de modificador de acréscimo ou de prefixo, a ação adicionará o valor a qualquer valor existente na variável.</span><span class="sxs-lookup"><span data-stu-id="70d92-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="70d92-133">0x2</span><span class="sxs-lookup"><span data-stu-id="70d92-133">0x2</span></span>       | <span data-ttu-id="70d92-134">Definido.</span><span class="sxs-lookup"><span data-stu-id="70d92-134">Set.</span></span> <span data-ttu-id="70d92-135">Define o valor se a variável estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="70d92-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="70d92-136">Se esse bit for combinado com um bit de modificador de acréscimo ou de prefixo, a ação adicionará o valor a qualquer valor existente na variável.</span><span class="sxs-lookup"><span data-stu-id="70d92-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="70d92-137">0x4</span><span class="sxs-lookup"><span data-stu-id="70d92-137">0x4</span></span>       | <span data-ttu-id="70d92-138">Remover.</span><span class="sxs-lookup"><span data-stu-id="70d92-138">Remove.</span></span> <span data-ttu-id="70d92-139">Remove o valor da variável.</span><span class="sxs-lookup"><span data-stu-id="70d92-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="70d92-140">Se esse bit for combinado com um bit de modificador de acréscimo ou de prefixo, o valor será removido da cadeia de caracteres existente, se o valor existir.</span><span class="sxs-lookup"><span data-stu-id="70d92-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="70d92-141">Valor de bit</span><span class="sxs-lookup"><span data-stu-id="70d92-141">Bit value</span></span>  | <span data-ttu-id="70d92-142">Descrição do modificador</span><span class="sxs-lookup"><span data-stu-id="70d92-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d92-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="70d92-143">0x20000000</span></span> | <span data-ttu-id="70d92-144">Se esse bit for definido, as ações serão aplicadas às variáveis de ambiente da máquina.</span><span class="sxs-lookup"><span data-stu-id="70d92-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="70d92-145">Se esse bit não estiver definido, as ações serão aplicadas às variáveis de ambiente do usuário.</span><span class="sxs-lookup"><span data-stu-id="70d92-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="70d92-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="70d92-146">0x40000000</span></span> | <span data-ttu-id="70d92-147">Anexar.</span><span class="sxs-lookup"><span data-stu-id="70d92-147">Append.</span></span> <span data-ttu-id="70d92-148">Esse bit é opcional.</span><span class="sxs-lookup"><span data-stu-id="70d92-148">This bit is optional.</span></span> <span data-ttu-id="70d92-149">Não defina os modificadores Append e Prefix.</span><span class="sxs-lookup"><span data-stu-id="70d92-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="70d92-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="70d92-150">0x80000000</span></span> | <span data-ttu-id="70d92-151">Prefixo.</span><span class="sxs-lookup"><span data-stu-id="70d92-151">Prefix.</span></span> <span data-ttu-id="70d92-152">Esse bit é opcional.</span><span class="sxs-lookup"><span data-stu-id="70d92-152">This bit is optional.</span></span> <span data-ttu-id="70d92-153">Não defina os modificadores Append e Prefix.</span><span class="sxs-lookup"><span data-stu-id="70d92-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




