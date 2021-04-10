---
description: ICE55 valida que todos os objetos LockPermission existem e têm valores de permissão válidos.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170840"
---
# <a name="ice55"></a><span data-ttu-id="e9bd8-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="e9bd8-103">ICE55</span></span>

<span data-ttu-id="e9bd8-104">ICE55 valida que todos os objetos LockPermission existem e têm valores de permissão válidos.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="e9bd8-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="e9bd8-105">Result</span></span>

<span data-ttu-id="e9bd8-106">ICE55 poste um erro se um lockobject listado na [Tabela LockPermissions](lockpermissions-table.md) não existir ou se nenhum nível de privilégio for especificado na coluna permissão.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="e9bd8-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e9bd8-107">Example</span></span>

<span data-ttu-id="e9bd8-108">ICE55 relataria os erros a seguir para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="e9bd8-109">[Tabela LockPermissions](lockpermissions-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e9bd8-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="e9bd8-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="e9bd8-110">LockObject</span></span> | <span data-ttu-id="e9bd8-111">Tabela</span><span class="sxs-lookup"><span data-stu-id="e9bd8-111">Table</span></span> | <span data-ttu-id="e9bd8-112">Domínio</span><span class="sxs-lookup"><span data-stu-id="e9bd8-112">Domain</span></span> | <span data-ttu-id="e9bd8-113">Usuário</span><span class="sxs-lookup"><span data-stu-id="e9bd8-113">User</span></span>  | <span data-ttu-id="e9bd8-114">Permissão</span><span class="sxs-lookup"><span data-stu-id="e9bd8-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="e9bd8-115">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="e9bd8-115">File1</span></span>      | <span data-ttu-id="e9bd8-116">Arquivo</span><span class="sxs-lookup"><span data-stu-id="e9bd8-116">File</span></span>  |        | <span data-ttu-id="e9bd8-117">guest</span><span class="sxs-lookup"><span data-stu-id="e9bd8-117">guest</span></span> |            |
| <span data-ttu-id="e9bd8-118">Arquivo3</span><span class="sxs-lookup"><span data-stu-id="e9bd8-118">File3</span></span>      | <span data-ttu-id="e9bd8-119">Arquivo</span><span class="sxs-lookup"><span data-stu-id="e9bd8-119">File</span></span>  |        | <span data-ttu-id="e9bd8-120">guest</span><span class="sxs-lookup"><span data-stu-id="e9bd8-120">guest</span></span> | <span data-ttu-id="e9bd8-121">1</span><span class="sxs-lookup"><span data-stu-id="e9bd8-121">1</span></span>          |



 

<span data-ttu-id="e9bd8-122">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e9bd8-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="e9bd8-123">Arquivo</span><span class="sxs-lookup"><span data-stu-id="e9bd8-123">File</span></span>  | <span data-ttu-id="e9bd8-124">Versão</span><span class="sxs-lookup"><span data-stu-id="e9bd8-124">Version</span></span> | <span data-ttu-id="e9bd8-125">Idioma</span><span class="sxs-lookup"><span data-stu-id="e9bd8-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="e9bd8-126">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="e9bd8-126">File1</span></span> | <span data-ttu-id="e9bd8-127">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="e9bd8-127">File2</span></span>   |          |
| <span data-ttu-id="e9bd8-128">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="e9bd8-128">File2</span></span> | <span data-ttu-id="e9bd8-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="e9bd8-129">1.0.0.0</span></span> | <span data-ttu-id="e9bd8-130">1046</span><span class="sxs-lookup"><span data-stu-id="e9bd8-130">1033</span></span>     |



 

<span data-ttu-id="e9bd8-131">O objeto arquivo1 tem um nulo na coluna de permissão.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="e9bd8-132">Cada linha deve ter um valor na coluna permissões.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="e9bd8-133">Para corrigir esse erro, especifique um valor numérico nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="e9bd8-134">Se nenhum privilégio for necessário para esse objeto, você deverá remover a linha.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="e9bd8-135">O objeto arquivo3 descrito na Tabela LockPermissions não está listado na tabela de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="e9bd8-136">Para corrigir esse erro, consulte um objeto válido.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9bd8-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9bd8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9bd8-138">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



