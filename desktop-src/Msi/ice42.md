---
description: ICE42 valida que os servidores InProc não estão vinculados a arquivos EXE na tabela de classes. Ele também valida que somente as classes LocalServer e LocalServer32 têm argumentos e valores DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752651"
---
# <a name="ice42"></a><span data-ttu-id="19b61-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="19b61-104">ICE42</span></span>

<span data-ttu-id="19b61-105">ICE42 valida que os servidores InProc não estão vinculados a arquivos EXE na [tabela de classes](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="19b61-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="19b61-106">Ele também valida que somente as classes LocalServer e LocalServer32 têm argumentos e valores DefInProc.</span><span class="sxs-lookup"><span data-stu-id="19b61-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="19b61-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="19b61-107">Result</span></span>

<span data-ttu-id="19b61-108">ICE42 posta um erro se houver servidores InProc vinculados a arquivos EXE na tabela de classes.</span><span class="sxs-lookup"><span data-stu-id="19b61-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="19b61-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="19b61-109">Example</span></span>

<span data-ttu-id="19b61-110">ICE42 relataria os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="19b61-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="19b61-111">Erro de ICE42</span><span class="sxs-lookup"><span data-stu-id="19b61-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="19b61-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="19b61-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b61-113">CLSID ' {GUID1} ' é um servidor InProc, mas o componente de implementação ' Component1 ' tem um EXE (' test.exe ') como KeyFile.</span><span class="sxs-lookup"><span data-stu-id="19b61-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="19b61-114">Há um arquivo executável especificado como um servidor InProc.</span><span class="sxs-lookup"><span data-stu-id="19b61-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="19b61-115">Os arquivos EXE não podem ser servidores InProc.</span><span class="sxs-lookup"><span data-stu-id="19b61-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="19b61-116">O CLSID ' {GUID1} ' no contexto ' InProcServer32 ' tem um argumento.</span><span class="sxs-lookup"><span data-stu-id="19b61-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="19b61-117">Somente contextos de LocalServer podem ter argumentos.</span><span class="sxs-lookup"><span data-stu-id="19b61-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="19b61-118">Para corrigir esse erro, remova o argumento.</span><span class="sxs-lookup"><span data-stu-id="19b61-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="19b61-119">CLSID ' {GUID1} ' no contexto ' InProcServer32 ' especifica um valor de InProc padrão.</span><span class="sxs-lookup"><span data-stu-id="19b61-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="19b61-120">Somente contextos de LocalServer podem ter valores de InProc padrão.</span><span class="sxs-lookup"><span data-stu-id="19b61-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="19b61-121">Há um objeto com um valor de InProc padrão que não é um objeto operando nos contextos LocalServer ou LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="19b61-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="19b61-122">Para corrigir esse erro, remova o valor DeflnProc ou altere o contexto da classe.</span><span class="sxs-lookup"><span data-stu-id="19b61-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="19b61-123">[Tabela de classes](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="19b61-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="19b61-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="19b61-124">CLSID</span></span>   | <span data-ttu-id="19b61-125">Contexto</span><span class="sxs-lookup"><span data-stu-id="19b61-125">Context</span></span>        | <span data-ttu-id="19b61-126">Componente\_</span><span class="sxs-lookup"><span data-stu-id="19b61-126">Component\_</span></span> | <span data-ttu-id="19b61-127">DefInProcHandler</span><span class="sxs-lookup"><span data-stu-id="19b61-127">DefInProcHandler</span></span> | <span data-ttu-id="19b61-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="19b61-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="19b61-129">GUID1</span><span class="sxs-lookup"><span data-stu-id="19b61-129">{GUID1}</span></span> | <span data-ttu-id="19b61-130">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="19b61-130">InProcServer32</span></span> | <span data-ttu-id="19b61-131">Component1</span><span class="sxs-lookup"><span data-stu-id="19b61-131">Component1</span></span>  | <span data-ttu-id="19b61-132">InProcServer</span><span class="sxs-lookup"><span data-stu-id="19b61-132">InProcServer</span></span>     | <span data-ttu-id="19b61-133">ARG</span><span class="sxs-lookup"><span data-stu-id="19b61-133">Arg</span></span>      |



 

<span data-ttu-id="19b61-134">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="19b61-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="19b61-135">Componente</span><span class="sxs-lookup"><span data-stu-id="19b61-135">Component</span></span>  | <span data-ttu-id="19b61-136">KeyPath</span><span class="sxs-lookup"><span data-stu-id="19b61-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="19b61-137">Component1</span><span class="sxs-lookup"><span data-stu-id="19b61-137">Component1</span></span> | <span data-ttu-id="19b61-138">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="19b61-138">File1</span></span>   |



 

<span data-ttu-id="19b61-139">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="19b61-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="19b61-140">Arquivo</span><span class="sxs-lookup"><span data-stu-id="19b61-140">File</span></span>  | <span data-ttu-id="19b61-141">Nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="19b61-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="19b61-142">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="19b61-142">File1</span></span> | <span data-ttu-id="19b61-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="19b61-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="19b61-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19b61-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b61-145">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="19b61-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




