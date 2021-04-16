---
description: Este exemplo permite que o consumidor do módulo configure de forma independente um controle de edição, o atributo checksum e o atributo compactado.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Exemplo de componente configurável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768476"
---
# <a name="configurable-component-example"></a><span data-ttu-id="0033f-103">Exemplo de componente configurável</span><span class="sxs-lookup"><span data-stu-id="0033f-103">Configurable Component Example</span></span>

<span data-ttu-id="0033f-104">Neste exemplo, as tabelas ModuleConfiguration e ModuleSubstitution a seguir permitem que o consumidor do módulo configure o atributo de senha de forma independente para um controle de edição, o atributo checksum de um arquivo e o atributo compactado para o mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="0033f-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="0033f-105">Tabela ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="0033f-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="0033f-106">Tabela</span><span class="sxs-lookup"><span data-stu-id="0033f-106">Table</span></span>   | <span data-ttu-id="0033f-107">Linha</span><span class="sxs-lookup"><span data-stu-id="0033f-107">Row</span></span>           | <span data-ttu-id="0033f-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="0033f-108">Column</span></span>     | <span data-ttu-id="0033f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0033f-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="0033f-110">Control</span><span class="sxs-lookup"><span data-stu-id="0033f-110">Control</span></span> | <span data-ttu-id="0033f-111">Dialog1; Edit1</span><span class="sxs-lookup"><span data-stu-id="0033f-111">Dialog1;Edit1</span></span> | <span data-ttu-id="0033f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="0033f-112">Attributes</span></span> | <span data-ttu-id="0033f-113">\[= Senha\]</span><span class="sxs-lookup"><span data-stu-id="0033f-113">\[=Password\]</span></span>                |
| <span data-ttu-id="0033f-114">Arquivo</span><span class="sxs-lookup"><span data-stu-id="0033f-114">File</span></span>    | <span data-ttu-id="0033f-115">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="0033f-115">File1</span></span>         | <span data-ttu-id="0033f-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="0033f-116">Attributes</span></span> | <span data-ttu-id="0033f-117">\[= Soma de verificação \] \[ = compactado\]</span><span class="sxs-lookup"><span data-stu-id="0033f-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="0033f-118">Tabela ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0033f-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="0033f-119">Nome</span><span class="sxs-lookup"><span data-stu-id="0033f-119">Name</span></span>       | <span data-ttu-id="0033f-120">Formatar</span><span class="sxs-lookup"><span data-stu-id="0033f-120">Format</span></span>   | <span data-ttu-id="0033f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0033f-121">Type</span></span> | <span data-ttu-id="0033f-122">ContextData</span><span class="sxs-lookup"><span data-stu-id="0033f-122">ContextData</span></span>                              | <span data-ttu-id="0033f-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0033f-123">DefaultValue</span></span> | <span data-ttu-id="0033f-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="0033f-124">Attributes</span></span> | <span data-ttu-id="0033f-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0033f-125">DisplayName</span></span> | <span data-ttu-id="0033f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="0033f-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="0033f-127">Senha</span><span class="sxs-lookup"><span data-stu-id="0033f-127">Password</span></span>   | <span data-ttu-id="0033f-128">Indevida</span><span class="sxs-lookup"><span data-stu-id="0033f-128">Bitfield</span></span> |      | <span data-ttu-id="0033f-129">2097152; True = 2097152; Falso = 0</span><span class="sxs-lookup"><span data-stu-id="0033f-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="0033f-130">0</span><span class="sxs-lookup"><span data-stu-id="0033f-130">0</span></span>            | <span data-ttu-id="0033f-131">0</span><span class="sxs-lookup"><span data-stu-id="0033f-131">0</span></span>          |             |             |
| <span data-ttu-id="0033f-132">Checksum (soma de verificação)</span><span class="sxs-lookup"><span data-stu-id="0033f-132">Checksum</span></span>   | <span data-ttu-id="0033f-133">Indevida</span><span class="sxs-lookup"><span data-stu-id="0033f-133">Bitfield</span></span> |      | <span data-ttu-id="0033f-134">1024; Soma de verificação = 1024; Nenhuma soma de verificação = 0</span><span class="sxs-lookup"><span data-stu-id="0033f-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="0033f-135">0</span><span class="sxs-lookup"><span data-stu-id="0033f-135">0</span></span>            | <span data-ttu-id="0033f-136">0</span><span class="sxs-lookup"><span data-stu-id="0033f-136">0</span></span>          |             |             |
| <span data-ttu-id="0033f-137">Compressed</span><span class="sxs-lookup"><span data-stu-id="0033f-137">Compressed</span></span> | <span data-ttu-id="0033f-138">Indevida</span><span class="sxs-lookup"><span data-stu-id="0033f-138">Bitfield</span></span> |      | <span data-ttu-id="0033f-139">24576; Compactado = 16384; Não compactado = 8192</span><span class="sxs-lookup"><span data-stu-id="0033f-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="0033f-140">8192</span><span class="sxs-lookup"><span data-stu-id="0033f-140">8192</span></span>         | <span data-ttu-id="0033f-141">0</span><span class="sxs-lookup"><span data-stu-id="0033f-141">0</span></span>          |             |             |



 

 

 



