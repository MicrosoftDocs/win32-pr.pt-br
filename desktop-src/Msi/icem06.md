---
description: ICEM06 verifica referências diretas inválidas para recursos pelo módulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828711"
---
# <a name="icem06"></a><span data-ttu-id="47cc2-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="47cc2-103">ICEM06</span></span>

<span data-ttu-id="47cc2-104">ICEM06 verifica referências diretas inválidas para recursos pelo módulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="47cc2-105">O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.</span><span class="sxs-lookup"><span data-stu-id="47cc2-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="47cc2-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="47cc2-106">Result</span></span>

<span data-ttu-id="47cc2-107">ICEM06 posta um erro quando o banco de dados do módulo contém referências diretas a um recurso.</span><span class="sxs-lookup"><span data-stu-id="47cc2-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="47cc2-108">As informações de recurso devem ser fornecidas pelo usuário do módulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="47cc2-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47cc2-109">Example</span></span>

<span data-ttu-id="47cc2-110">ICEM06 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="47cc2-111">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="47cc2-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="47cc2-112">Atalho</span><span class="sxs-lookup"><span data-stu-id="47cc2-112">Shortcut</span></span>          | <span data-ttu-id="47cc2-113">Destino</span><span class="sxs-lookup"><span data-stu-id="47cc2-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="47cc2-114">Shortcut1. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="47cc2-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="47cc2-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="47cc2-115">cmd.exe</span></span>                                |
| <span data-ttu-id="47cc2-116">Shortcut2. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="47cc2-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="47cc2-117">\[MyProp\]</span><span class="sxs-lookup"><span data-stu-id="47cc2-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="47cc2-118">Shortcut3. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="47cc2-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="47cc2-119">[Tabela de classes](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="47cc2-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="47cc2-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="47cc2-120">CLSID</span></span>   | <span data-ttu-id="47cc2-121">Contexto</span><span class="sxs-lookup"><span data-stu-id="47cc2-121">Context</span></span>       | <span data-ttu-id="47cc2-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="47cc2-122">Component\_</span></span> | <span data-ttu-id="47cc2-123">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="47cc2-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="47cc2-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="47cc2-124">*GUID1*</span></span> | <span data-ttu-id="47cc2-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="47cc2-125">LocalServer32</span></span> | <span data-ttu-id="47cc2-126">Component1</span><span class="sxs-lookup"><span data-stu-id="47cc2-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="47cc2-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="47cc2-127">*GUID2*</span></span> | <span data-ttu-id="47cc2-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="47cc2-128">LocalServer32</span></span> | <span data-ttu-id="47cc2-129">Component2</span><span class="sxs-lookup"><span data-stu-id="47cc2-129">Component2</span></span>  | <span data-ttu-id="47cc2-130">MyFeature</span><span class="sxs-lookup"><span data-stu-id="47cc2-130">MyFeature</span></span>                              |



 

<span data-ttu-id="47cc2-131">O ICEM06 relata o primeiro erro porque o primeiro registro na tabela de atalho tem uma entrada no campo de destino que não é uma propriedade ou um GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="47cc2-132">Um módulo não pode fazer referência diretamente a um recurso.</span><span class="sxs-lookup"><span data-stu-id="47cc2-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="47cc2-133">As informações de recurso devem ser fornecidas pelo usuário do módulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="47cc2-134">Para corrigir esse erro, as referências a um recurso devem ser substituídas por um GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="47cc2-135">ICEM06 relata o segundo erro porque o segundo registro na tabela de classes tem uma entrada no campo de recurso que não é um GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="47cc2-136">Um módulo não pode fazer referência diretamente a um recurso.</span><span class="sxs-lookup"><span data-stu-id="47cc2-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="47cc2-137">As informações de recurso devem ser fornecidas pelo usuário do módulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="47cc2-138">Para corrigir esse erro, as referências a um recurso devem ser substituídas por um GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="47cc2-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47cc2-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47cc2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47cc2-140">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="47cc2-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



