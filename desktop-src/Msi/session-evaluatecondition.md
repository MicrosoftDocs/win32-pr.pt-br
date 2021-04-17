---
description: O método EvaluateCondition do objeto Session avalia uma expressão lógica que contém símbolos e valores. Esse método usa a função MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Método Session. EvaluateCondition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759375"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="82577-104">Método Session. EvaluateCondition</span><span class="sxs-lookup"><span data-stu-id="82577-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="82577-105">O método **EvaluateCondition** do objeto [**Session**](session-object.md) avalia uma expressão lógica que contém símbolos e valores.</span><span class="sxs-lookup"><span data-stu-id="82577-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="82577-106">Esse método usa a função [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="82577-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="82577-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82577-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="82577-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82577-109">*problema*</span><span class="sxs-lookup"><span data-stu-id="82577-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="82577-110">Cadeia de caracteres necessária que contém a expressão lógica.</span><span class="sxs-lookup"><span data-stu-id="82577-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="82577-111">Para obter mais informações, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="82577-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82577-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82577-112">Return value</span></span>

<span data-ttu-id="82577-113">Esse método retorna um inteiro que indica a avaliação da condição.</span><span class="sxs-lookup"><span data-stu-id="82577-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="82577-114">Constante</span><span class="sxs-lookup"><span data-stu-id="82577-114">Constant</span></span>                  | <span data-ttu-id="82577-115">Valor</span><span class="sxs-lookup"><span data-stu-id="82577-115">Value</span></span> | <span data-ttu-id="82577-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="82577-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="82577-117">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="82577-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="82577-118">0</span><span class="sxs-lookup"><span data-stu-id="82577-118">0</span></span>     | <span data-ttu-id="82577-119">A condição é avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="82577-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="82577-120">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="82577-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="82577-121">1</span><span class="sxs-lookup"><span data-stu-id="82577-121">1</span></span>     | <span data-ttu-id="82577-122">A condição é avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="82577-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="82577-123">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="82577-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="82577-124">2</span><span class="sxs-lookup"><span data-stu-id="82577-124">2</span></span>     | <span data-ttu-id="82577-125">Uma expressão condicional não é fornecida.</span><span class="sxs-lookup"><span data-stu-id="82577-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="82577-126">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="82577-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="82577-127">3</span><span class="sxs-lookup"><span data-stu-id="82577-127">3</span></span>     | <span data-ttu-id="82577-128">A condição contém um erro de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="82577-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="82577-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="82577-129">Remarks</span></span>

<span data-ttu-id="82577-130">Expressões condicionais podem ser usadas para comparar Estados de recursos e componentes.</span><span class="sxs-lookup"><span data-stu-id="82577-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="82577-131">A tabela a seguir mostra o recurso e os Estados de componente que o método EvaluateCondition usa.</span><span class="sxs-lookup"><span data-stu-id="82577-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="82577-132">Estado</span><span class="sxs-lookup"><span data-stu-id="82577-132">State</span></span>                 | <span data-ttu-id="82577-133">Valor</span><span class="sxs-lookup"><span data-stu-id="82577-133">Value</span></span> | <span data-ttu-id="82577-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="82577-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="82577-135">Nulo</span><span class="sxs-lookup"><span data-stu-id="82577-135">Null</span></span>                  | <span data-ttu-id="82577-136">Nulo</span><span class="sxs-lookup"><span data-stu-id="82577-136">Null</span></span>  | <span data-ttu-id="82577-137">Nenhuma ação executada no recurso ou componente.</span><span class="sxs-lookup"><span data-stu-id="82577-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="82577-138">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="82577-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="82577-139">2</span><span class="sxs-lookup"><span data-stu-id="82577-139">2</span></span>     | <span data-ttu-id="82577-140">O recurso ou componente não está presente.</span><span class="sxs-lookup"><span data-stu-id="82577-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="82577-141">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="82577-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="82577-142">3</span><span class="sxs-lookup"><span data-stu-id="82577-142">3</span></span>     | <span data-ttu-id="82577-143">O recurso ou componente está instalado no computador local.</span><span class="sxs-lookup"><span data-stu-id="82577-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="82577-144">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="82577-144">msiInstallStateSource</span></span> | <span data-ttu-id="82577-145">4</span><span class="sxs-lookup"><span data-stu-id="82577-145">4</span></span>     | <span data-ttu-id="82577-146">O recurso ou componente está instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="82577-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="82577-147">Os Estados não são definidos até que o método [**SetInstallLevel**](session-setinstalllevel.md) seja chamado, seja diretamente ou pela [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="82577-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="82577-148">Portanto, a verificação de estado só é útil em expressão condicional em uma tabela de sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="82577-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82577-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82577-149">Requirements</span></span>



| <span data-ttu-id="82577-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="82577-150">Requirement</span></span> | <span data-ttu-id="82577-151">Valor</span><span class="sxs-lookup"><span data-stu-id="82577-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82577-152">Versão</span><span class="sxs-lookup"><span data-stu-id="82577-152">Version</span></span><br/> | <span data-ttu-id="82577-153">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82577-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82577-154">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82577-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82577-155">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="82577-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="82577-156">DLL</span><span class="sxs-lookup"><span data-stu-id="82577-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="82577-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82577-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="82577-158">IID</span><span class="sxs-lookup"><span data-stu-id="82577-158">IID</span></span><br/>     | <span data-ttu-id="82577-159">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="82577-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="82577-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="82577-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82577-161">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="82577-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




