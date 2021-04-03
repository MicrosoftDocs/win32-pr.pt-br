---
description: ICE40 faz uma validação diversas.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091732"
---
# <a name="ice40"></a><span data-ttu-id="b8e93-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="b8e93-103">ICE40</span></span>

<span data-ttu-id="b8e93-104">ICE40 faz uma validação diversas.</span><span class="sxs-lookup"><span data-stu-id="b8e93-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="b8e93-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="b8e93-105">Result</span></span>

<span data-ttu-id="b8e93-106">O ICE40 posta avisos sobre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b8e93-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="b8e93-107">A propriedade [**REinstallmode**](reinstallmode.md) foi substituída.</span><span class="sxs-lookup"><span data-stu-id="b8e93-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="b8e93-108">A [tabela RemoveIniFile](removeinifile-table.md) tem uma entrada Delete tag sem valor.</span><span class="sxs-lookup"><span data-stu-id="b8e93-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="b8e93-109">O arquivo. msi não tem a [tabela de erros](error-table.md) e a propriedade de [**Resumo de contagem de páginas**](page-count-summary.md) é menor ou igual a 100.</span><span class="sxs-lookup"><span data-stu-id="b8e93-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="b8e93-110">Este aviso de gelo está obsoleto porque Windows Installer não exige que o pacote tenha uma tabela de erro.</span><span class="sxs-lookup"><span data-stu-id="b8e93-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="b8e93-111">As mensagens de erro podem ser recuperadas usando Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="b8e93-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="b8e93-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b8e93-112">Example</span></span>

[<span data-ttu-id="b8e93-113">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="b8e93-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="b8e93-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b8e93-114">Property</span></span>                               | <span data-ttu-id="b8e93-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b8e93-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="b8e93-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="b8e93-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="b8e93-117">Um</span><span class="sxs-lookup"><span data-stu-id="b8e93-117">A</span></span>     |



 

[<span data-ttu-id="b8e93-118">Tabela RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="b8e93-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="b8e93-119">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="b8e93-119">RemoveIniFile</span></span>                          | <span data-ttu-id="b8e93-120">Ação</span><span class="sxs-lookup"><span data-stu-id="b8e93-120">Action</span></span> | <span data-ttu-id="b8e93-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b8e93-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="b8e93-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="b8e93-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="b8e93-123">4</span><span class="sxs-lookup"><span data-stu-id="b8e93-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="b8e93-124">Resultados</span><span class="sxs-lookup"><span data-stu-id="b8e93-124">Results</span></span>

<span data-ttu-id="b8e93-125">ICE40 relataria os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8e93-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="b8e93-126">Erro de ICE40</span><span class="sxs-lookup"><span data-stu-id="b8e93-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="b8e93-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8e93-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e93-128">[**REinstallmode**](reinstallmode.md) é definido na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8e93-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="b8e93-129">Isso pode causar dificuldades.</span><span class="sxs-lookup"><span data-stu-id="b8e93-129">This may cause difficulties.</span></span> | <span data-ttu-id="b8e93-130">Definir a propriedade [**REinstallmode**](reinstallmode.md) no arquivo. msi pode levar a um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="b8e93-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="b8e93-131">Para corrigir esse erro, não defina essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b8e93-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b8e93-132">A entrada RemoveIniFile Remove1 deve ter um valor, pois a ação é "excluir marca" (4).</span><span class="sxs-lookup"><span data-stu-id="b8e93-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="b8e93-133">Há uma ação DELETE tag no na coluna RemoveIniFile da [tabela RemoveIniFile](removeinifile-table.md) sem especificar uma marca a ser excluída na coluna Value.</span><span class="sxs-lookup"><span data-stu-id="b8e93-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b8e93-134">A tabela de erros está ausente.</span><span class="sxs-lookup"><span data-stu-id="b8e93-134">Error Table is missing.</span></span> <span data-ttu-id="b8e93-135">Serão geradas apenas mensagens de erro numéricas.</span><span class="sxs-lookup"><span data-stu-id="b8e93-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="b8e93-136">Este aviso de gelo está obsoleto porque Windows Installer não exige que o pacote tenha uma [tabela de erro](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="b8e93-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="b8e93-137">As mensagens de erro podem ser recuperadas usando Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="b8e93-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="b8e93-138">Esse aviso significa que o arquivo. msi não tem a [tabela de erros](error-table.md) e a propriedade de [**Resumo de contagem de páginas**](page-count-summary.md) é menor ou igual a 100.</span><span class="sxs-lookup"><span data-stu-id="b8e93-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="b8e93-139">Para corrigir esse erro, use uma versão atual do Windows Installer ou adicione uma tabela de erros ao pacote de instalação e crie modelos de formatação na coluna mensagem para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="b8e93-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b8e93-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8e93-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e93-141">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="b8e93-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




