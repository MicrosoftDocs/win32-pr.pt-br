---
title: opção/n
description: A opção/n especifica a profundidade da composição para compor arquivos de metadados.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n alternar MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768736"
---
# <a name="n-switch"></a><span data-ttu-id="b91dd-104">opção/n</span><span class="sxs-lookup"><span data-stu-id="b91dd-104">/n switch</span></span>

<span data-ttu-id="b91dd-105">A opção **/n** especifica a profundidade da composição para compor arquivos de metadados.</span><span class="sxs-lookup"><span data-stu-id="b91dd-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="b91dd-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="b91dd-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b91dd-107">*profundidade do namespace \_*</span><span class="sxs-lookup"><span data-stu-id="b91dd-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="b91dd-108">Especifica a profundidade do namespace a ser redigida em um único arquivo de metadados.</span><span class="sxs-lookup"><span data-stu-id="b91dd-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b91dd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b91dd-109">Remarks</span></span>

<span data-ttu-id="b91dd-110">Aqui estão os formatos de valor possíveis que você pode especificar com a opção **/n** .</span><span class="sxs-lookup"><span data-stu-id="b91dd-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="b91dd-111">Formato de valor</span><span class="sxs-lookup"><span data-stu-id="b91dd-111">Value format</span></span>                   | <span data-ttu-id="b91dd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b91dd-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b91dd-113">Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="b91dd-113">Int32 > 0</span></span>                   | <span data-ttu-id="b91dd-114">Compor todos os tipos na profundidade do namespace especificada na opção.</span><span class="sxs-lookup"><span data-stu-id="b91dd-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="b91dd-115">-1</span><span class="sxs-lookup"><span data-stu-id="b91dd-115">-1</span></span>                             | <span data-ttu-id="b91dd-116">Compor todos os tipos em um arquivo IDL por namespace.</span><span class="sxs-lookup"><span data-stu-id="b91dd-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="b91dd-117"><namespace>: Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="b91dd-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="b91dd-118">Compor todos os tipos com namespace correspondente na profundidade especificada na opção.</span><span class="sxs-lookup"><span data-stu-id="b91dd-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="b91dd-119"><namespace>:-1</span><span class="sxs-lookup"><span data-stu-id="b91dd-119"><namespace>:-1</span></span>           | <span data-ttu-id="b91dd-120">Compor todos os tipos com namespace correspondente em um arquivo por namespace.</span><span class="sxs-lookup"><span data-stu-id="b91dd-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="b91dd-121">A tabela a seguir mostra os resultados de diferentes combinações da opção **/n** trabalhando nesses namespaces.</span><span class="sxs-lookup"><span data-stu-id="b91dd-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="b91dd-122">Windows. Foundation. Collections. IIterable</span><span class="sxs-lookup"><span data-stu-id="b91dd-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="b91dd-123">Windows. UI. DirectUI. Controls. Button</span><span class="sxs-lookup"><span data-stu-id="b91dd-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="b91dd-124">Windows. UI. DirectUI. Controls. ListView</span><span class="sxs-lookup"><span data-stu-id="b91dd-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="b91dd-125">Windows. UI. imersão. Application. Playto. Target</span><span class="sxs-lookup"><span data-stu-id="b91dd-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="b91dd-126">Windows. Web. Syndication. RSS</span><span class="sxs-lookup"><span data-stu-id="b91dd-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="b91dd-127">Comutadores</span><span class="sxs-lookup"><span data-stu-id="b91dd-127">Switches</span></span>                         | <span data-ttu-id="b91dd-128">Resultado</span><span class="sxs-lookup"><span data-stu-id="b91dd-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="b91dd-129">Explicação</span><span class="sxs-lookup"><span data-stu-id="b91dd-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91dd-130">**/n:-1**  / **n:1**</span><span class="sxs-lookup"><span data-stu-id="b91dd-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="b91dd-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="b91dd-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="b91dd-132">A última opção/n substitui todas as opções-n anteriores.</span><span class="sxs-lookup"><span data-stu-id="b91dd-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b91dd-133">**/n:-1/n: Windows. UI: 2**</span><span class="sxs-lookup"><span data-stu-id="b91dd-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="b91dd-134">Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. Winmd</dt> <dt>Windows. Web. Syndication. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="b91dd-135"><dt>O **Windows. Foundation** é sempre composto em – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="b91dd-136"><dt>Os tipos **Windows. UI** são agrupados.</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="b91dd-137"><dt>O **Windows. Web. Syndication** é composto em n:-1.</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="b91dd-138">**/n: 1/n: Windows. UI. DirectUI: 3**</span><span class="sxs-lookup"><span data-stu-id="b91dd-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="b91dd-139">Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. DirectUI. winmd</dt> <dt>Windows. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="b91dd-140"><dt>O **Windows. Foundation** é sempre composto em – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="b91dd-141"><dt>**Windows. UI. DirectUI** é composto no nível 3.</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="b91dd-142"><dt>Todos os outros tipos são compostos no nível 1.</dt></span><span class="sxs-lookup"><span data-stu-id="b91dd-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="b91dd-143">Aqui estão as regras para lidar com várias instâncias da opção **/n** .</span><span class="sxs-lookup"><span data-stu-id="b91dd-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="b91dd-144">A instância mais específica prevalece.</span><span class="sxs-lookup"><span data-stu-id="b91dd-144">The most specific instance prevails.</span></span> <span data-ttu-id="b91dd-145">Por exemplo, se você especificar **– n:A.B.C: 4 – n:A.B: 5**, MDMERGE resolverá a. b. c. D no nível 4, porque A. b. c é mais específica que A.B.</span><span class="sxs-lookup"><span data-stu-id="b91dd-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="b91dd-146">A. B. E. F resolve na profundidade 5, porque corresponde A. B, mas não A.B.C.</span><span class="sxs-lookup"><span data-stu-id="b91dd-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="b91dd-147">A última instância prevalece.</span><span class="sxs-lookup"><span data-stu-id="b91dd-147">The last instance prevails.</span></span> <span data-ttu-id="b91dd-148">Por exemplo, se você especificar **– n:5 – n:2**, os tipos serão compostos no nível 2.</span><span class="sxs-lookup"><span data-stu-id="b91dd-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="b91dd-149">Ambas as regras se aplicam.</span><span class="sxs-lookup"><span data-stu-id="b91dd-149">Both of these rules apply.</span></span> <span data-ttu-id="b91dd-150">Se você especificar – n:A.B.C: 4 – n:A.B.C: 1, namespace A. B. C é composto no nível 1.</span><span class="sxs-lookup"><span data-stu-id="b91dd-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="b91dd-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b91dd-151">Examples</span></span>

<span data-ttu-id="b91dd-152">**mdmerge.exe-metadados \_ dir $ (caminho de metadados do SDK \_ \_ )-i $ ( \_ caminho de metadados do SDK interno \_ \_ )-o $ (caminho do obj \_ ) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation: 2**</span><span class="sxs-lookup"><span data-stu-id="b91dd-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="b91dd-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b91dd-153">Requirements</span></span>



| <span data-ttu-id="b91dd-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91dd-154">Requirement</span></span> | <span data-ttu-id="b91dd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="b91dd-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="b91dd-156">Cliente</span><span class="sxs-lookup"><span data-stu-id="b91dd-156">Client</span></span><br/> | <span data-ttu-id="b91dd-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b91dd-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="b91dd-158">Servidor</span><span class="sxs-lookup"><span data-stu-id="b91dd-158">Server</span></span><br/> | <span data-ttu-id="b91dd-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b91dd-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b91dd-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="b91dd-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91dd-161">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="b91dd-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





