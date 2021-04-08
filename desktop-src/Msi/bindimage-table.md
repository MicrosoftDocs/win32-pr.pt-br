---
description: A tabela BindImage contém informações sobre cada executável ou DLL que precisa ser associado às DLLs importadas por ele.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabela BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921483"
---
# <a name="bindimage-table"></a><span data-ttu-id="cfc59-103">Tabela BindImage</span><span class="sxs-lookup"><span data-stu-id="cfc59-103">BindImage Table</span></span>

<span data-ttu-id="cfc59-104">A tabela BindImage contém informações sobre cada executável ou DLL que precisa ser associado às DLLs importadas por ele.</span><span class="sxs-lookup"><span data-stu-id="cfc59-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="cfc59-105">A tabela BindImage tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="cfc59-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="cfc59-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="cfc59-106">Column</span></span> | <span data-ttu-id="cfc59-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="cfc59-107">Type</span></span>                         | <span data-ttu-id="cfc59-108">Chave</span><span class="sxs-lookup"><span data-stu-id="cfc59-108">Key</span></span> | <span data-ttu-id="cfc59-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="cfc59-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="cfc59-110">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="cfc59-110">File\_</span></span> | [<span data-ttu-id="cfc59-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="cfc59-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="cfc59-112">S</span><span class="sxs-lookup"><span data-stu-id="cfc59-112">Y</span></span>   | <span data-ttu-id="cfc59-113">N</span><span class="sxs-lookup"><span data-stu-id="cfc59-113">N</span></span>        |
| <span data-ttu-id="cfc59-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="cfc59-114">Path</span></span>   | [<span data-ttu-id="cfc59-115">Caminhos</span><span class="sxs-lookup"><span data-stu-id="cfc59-115">Paths</span></span>](paths.md)           | <span data-ttu-id="cfc59-116">N</span><span class="sxs-lookup"><span data-stu-id="cfc59-116">N</span></span>   | <span data-ttu-id="cfc59-117">S</span><span class="sxs-lookup"><span data-stu-id="cfc59-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cfc59-118">Colunas</span><span class="sxs-lookup"><span data-stu-id="cfc59-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cfc59-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="cfc59-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="cfc59-120">Uma chave externa para a coluna um da [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="cfc59-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="cfc59-121">Esse deve ser um arquivo executável ou um arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="cfc59-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="cfc59-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Multi-Path</span><span class="sxs-lookup"><span data-stu-id="cfc59-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="cfc59-123">Uma lista de caminhos, separados por ponto e vírgula, que representam os caminhos a serem pesquisados para localizar as DLLs importadas.</span><span class="sxs-lookup"><span data-stu-id="cfc59-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="cfc59-124">A lista geralmente é uma lista de propriedades, com cada propriedade delimitada entre colchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="cfc59-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cfc59-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfc59-125">Remarks</span></span>

<span data-ttu-id="cfc59-126">O instalador computa o endereço virtual de cada função importada de todas as DLLs, e o endereço virtual computado é salvo na tabela de endereços de importação da imagem de importação (IAT).</span><span class="sxs-lookup"><span data-stu-id="cfc59-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="cfc59-127">Essa tabela é referida quando a [ação de BindImage](bindimage-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="cfc59-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="cfc59-128">Validação</span><span class="sxs-lookup"><span data-stu-id="cfc59-128">Validation</span></span>

<dl>

[<span data-ttu-id="cfc59-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="cfc59-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cfc59-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="cfc59-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cfc59-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="cfc59-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="cfc59-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="cfc59-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="cfc59-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="cfc59-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



