---
description: Ações personalizadas escritas em JScript ou Visual Basic, Scripting Edition (VBScript) podem chamar uma função opcional. Essas funções devem retornar um dos valores mostrados na tabela a seguir.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valores de retorno de ações personalizadas do JScript e do VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753260"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="ab6b6-104">Valores de retorno de ações personalizadas do JScript e do VBScript</span><span class="sxs-lookup"><span data-stu-id="ab6b6-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="ab6b6-105">Ações personalizadas escritas em JScript ou Visual Basic, Scripting Edition (VBScript) podem chamar uma função opcional.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="ab6b6-106">Essas funções devem retornar um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="ab6b6-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab6b6-107">Return value</span></span>              | <span data-ttu-id="ab6b6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ab6b6-108">Value</span></span>        | <span data-ttu-id="ab6b6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab6b6-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6b6-110">msiDoActionStatusNoAction</span><span class="sxs-lookup"><span data-stu-id="ab6b6-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="ab6b6-111">0</span><span class="sxs-lookup"><span data-stu-id="ab6b6-111">0</span></span>            | <span data-ttu-id="ab6b6-112">Ação não executada.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="ab6b6-113">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="ab6b6-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="ab6b6-114">IDOK = 1</span><span class="sxs-lookup"><span data-stu-id="ab6b6-114">IDOK = 1</span></span>     | <span data-ttu-id="ab6b6-115">Ação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="ab6b6-116">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="ab6b6-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="ab6b6-117">IDCANCEL = 2</span><span class="sxs-lookup"><span data-stu-id="ab6b6-117">IDCANCEL = 2</span></span> | <span data-ttu-id="ab6b6-118">Encerramento prematuro pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="ab6b6-119">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="ab6b6-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="ab6b6-120">IDABORT = 3</span><span class="sxs-lookup"><span data-stu-id="ab6b6-120">IDABORT = 3</span></span>  | <span data-ttu-id="ab6b6-121">Erro irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-121">Unrecoverable error.</span></span> <span data-ttu-id="ab6b6-122">Retornado se houver um erro durante a análise ou execução do JScript ou VBScript.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="ab6b6-123">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="ab6b6-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="ab6b6-124">IDRETRY = 4</span><span class="sxs-lookup"><span data-stu-id="ab6b6-124">IDRETRY = 4</span></span>  | <span data-ttu-id="ab6b6-125">Sequência suspensa a ser retomada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="ab6b6-126">msiDoActionStatusFinished</span><span class="sxs-lookup"><span data-stu-id="ab6b6-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="ab6b6-127">IDIGNORE = 5</span><span class="sxs-lookup"><span data-stu-id="ab6b6-127">IDIGNORE = 5</span></span> | <span data-ttu-id="ab6b6-128">Ignorar as ações restantes.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-128">Skip remaining actions.</span></span> <span data-ttu-id="ab6b6-129">Não é um erro.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="ab6b6-130">Observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="ab6b6-131">Por exemplo, se o valor de retorno da ação aparecer como 1 (um) no arquivo de log, isso significa que a ação retornou msiDoActionStatusSuccess.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="ab6b6-132">Para obter mais informações sobre essa conversão, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ab6b6-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="ab6b6-133">Para retornar um valor diferente de êxito de uma ação personalizada de script, você deve usar um destino de função para a ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="ab6b6-134">A função de destino é especificada na coluna de destino da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab6b6-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="ab6b6-135">O exemplo de script a seguir mostra como retornar êxito ou falha de uma ação personalizada do VBScript.</span><span class="sxs-lookup"><span data-stu-id="ab6b6-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="ab6b6-136">Se esse VBScript tiver sido inserido na [tabela binária](binary-table.md) do pacote de instalação como MyCA.vbs, a entrada da [tabela CustomAction](customaction-table.md) para o script será a seguinte:</span><span class="sxs-lookup"><span data-stu-id="ab6b6-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="ab6b6-137">Ação</span><span class="sxs-lookup"><span data-stu-id="ab6b6-137">Action</span></span>         | <span data-ttu-id="ab6b6-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab6b6-138">Type</span></span> | <span data-ttu-id="ab6b6-139">Fonte</span><span class="sxs-lookup"><span data-stu-id="ab6b6-139">Source</span></span>   | <span data-ttu-id="ab6b6-140">Destino</span><span class="sxs-lookup"><span data-stu-id="ab6b6-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="ab6b6-141">Mycustomizable</span><span class="sxs-lookup"><span data-stu-id="ab6b6-141">MyCustomAction</span></span> | <span data-ttu-id="ab6b6-142">6</span><span class="sxs-lookup"><span data-stu-id="ab6b6-142">6</span></span>    | <span data-ttu-id="ab6b6-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="ab6b6-143">MyCA.vbs</span></span> | <span data-ttu-id="ab6b6-144">MyVBScriptCA</span><span class="sxs-lookup"><span data-stu-id="ab6b6-144">MyVBScriptCA</span></span> |



 

 

 



