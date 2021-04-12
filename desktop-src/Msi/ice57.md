---
description: O ICE57 valida que componentes individuais não misturam dados por computador e por usuário. Essa ação personalizada de ICE verifica entradas de registro, arquivos, caminhos de chave de diretório e atalhos não anunciados.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170839"
---
# <a name="ice57"></a><span data-ttu-id="8fecf-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="8fecf-104">ICE57</span></span>

<span data-ttu-id="8fecf-105">O ICE57 valida que componentes individuais não misturam dados por computador e por usuário.</span><span class="sxs-lookup"><span data-stu-id="8fecf-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="8fecf-106">Essa ação personalizada de ICE verifica entradas de registro, arquivos, caminhos de chave de diretório e atalhos não anunciados.</span><span class="sxs-lookup"><span data-stu-id="8fecf-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="8fecf-107">A combinação de dados por usuário e por computador no mesmo componente pode resultar na instalação parcial do componente para alguns usuários em um ambiente de vários usuários.</span><span class="sxs-lookup"><span data-stu-id="8fecf-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="8fecf-108">Consulte a propriedade [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="8fecf-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="8fecf-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="8fecf-109">Result</span></span>

<span data-ttu-id="8fecf-110">O ICE57 posta um erro se encontrar algum componente que contenha entradas de registro por computador e por usuário, arquivos, caminhos de chave de diretório ou atalhos não anunciados.</span><span class="sxs-lookup"><span data-stu-id="8fecf-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="8fecf-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8fecf-111">Example</span></span>

<span data-ttu-id="8fecf-112">ICE57reports os seguintes erros para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="8fecf-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="8fecf-113">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8fecf-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="8fecf-114">Componente</span><span class="sxs-lookup"><span data-stu-id="8fecf-114">Component</span></span>  | <span data-ttu-id="8fecf-115">Diretório</span><span class="sxs-lookup"><span data-stu-id="8fecf-115">Directory</span></span>  | <span data-ttu-id="8fecf-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="8fecf-116">Attributes</span></span> | <span data-ttu-id="8fecf-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="8fecf-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="8fecf-118">Component1</span><span class="sxs-lookup"><span data-stu-id="8fecf-118">Component1</span></span> | <span data-ttu-id="8fecf-119">Directorya</span><span class="sxs-lookup"><span data-stu-id="8fecf-119">DirectoryA</span></span> | <span data-ttu-id="8fecf-120">0</span><span class="sxs-lookup"><span data-stu-id="8fecf-120">0</span></span>          | <span data-ttu-id="8fecf-121">FileA</span><span class="sxs-lookup"><span data-stu-id="8fecf-121">FileA</span></span>   |
| <span data-ttu-id="8fecf-122">Component2</span><span class="sxs-lookup"><span data-stu-id="8fecf-122">Component2</span></span> | <span data-ttu-id="8fecf-123">Directorya</span><span class="sxs-lookup"><span data-stu-id="8fecf-123">DirectoryA</span></span> | <span data-ttu-id="8fecf-124">4</span><span class="sxs-lookup"><span data-stu-id="8fecf-124">4</span></span>          | <span data-ttu-id="8fecf-125">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="8fecf-125">RegKeyB</span></span> |
| <span data-ttu-id="8fecf-126">Component3</span><span class="sxs-lookup"><span data-stu-id="8fecf-126">Component3</span></span> | <span data-ttu-id="8fecf-127">Directorya</span><span class="sxs-lookup"><span data-stu-id="8fecf-127">DirectoryA</span></span> | <span data-ttu-id="8fecf-128">0</span><span class="sxs-lookup"><span data-stu-id="8fecf-128">0</span></span>          | <span data-ttu-id="8fecf-129">FileC</span><span class="sxs-lookup"><span data-stu-id="8fecf-129">FileC</span></span>   |
| <span data-ttu-id="8fecf-130">Component4</span><span class="sxs-lookup"><span data-stu-id="8fecf-130">Component4</span></span> | <span data-ttu-id="8fecf-131">Directorya</span><span class="sxs-lookup"><span data-stu-id="8fecf-131">DirectoryA</span></span> | <span data-ttu-id="8fecf-132">4</span><span class="sxs-lookup"><span data-stu-id="8fecf-132">4</span></span>          | <span data-ttu-id="8fecf-133">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="8fecf-133">RegKeyD</span></span> |



 

<span data-ttu-id="8fecf-134">[Tabela do registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8fecf-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="8fecf-135">Registro</span><span class="sxs-lookup"><span data-stu-id="8fecf-135">Registry</span></span> | <span data-ttu-id="8fecf-136">Root</span><span class="sxs-lookup"><span data-stu-id="8fecf-136">Root</span></span> | <span data-ttu-id="8fecf-137">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8fecf-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="8fecf-138">RegKeyA</span><span class="sxs-lookup"><span data-stu-id="8fecf-138">RegKeyA</span></span>  | <span data-ttu-id="8fecf-139">1</span><span class="sxs-lookup"><span data-stu-id="8fecf-139">1</span></span>    | <span data-ttu-id="8fecf-140">Component1</span><span class="sxs-lookup"><span data-stu-id="8fecf-140">Component1</span></span>  |
| <span data-ttu-id="8fecf-141">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="8fecf-141">RegKeyB</span></span>  | <span data-ttu-id="8fecf-142">1</span><span class="sxs-lookup"><span data-stu-id="8fecf-142">1</span></span>    | <span data-ttu-id="8fecf-143">Component2</span><span class="sxs-lookup"><span data-stu-id="8fecf-143">Component2</span></span>  |
| <span data-ttu-id="8fecf-144">RegKeyC</span><span class="sxs-lookup"><span data-stu-id="8fecf-144">RegKeyC</span></span>  | <span data-ttu-id="8fecf-145">-1</span><span class="sxs-lookup"><span data-stu-id="8fecf-145">-1</span></span>   | <span data-ttu-id="8fecf-146">Component3</span><span class="sxs-lookup"><span data-stu-id="8fecf-146">Component3</span></span>  |
| <span data-ttu-id="8fecf-147">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="8fecf-147">RegKeyD</span></span>  | <span data-ttu-id="8fecf-148">-1</span><span class="sxs-lookup"><span data-stu-id="8fecf-148">-1</span></span>   | <span data-ttu-id="8fecf-149">Component4</span><span class="sxs-lookup"><span data-stu-id="8fecf-149">Component4</span></span>  |



 

<span data-ttu-id="8fecf-150">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8fecf-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="8fecf-151">Arquivo</span><span class="sxs-lookup"><span data-stu-id="8fecf-151">File</span></span>  | <span data-ttu-id="8fecf-152">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8fecf-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="8fecf-153">FileA</span><span class="sxs-lookup"><span data-stu-id="8fecf-153">FileA</span></span> | <span data-ttu-id="8fecf-154">Component1</span><span class="sxs-lookup"><span data-stu-id="8fecf-154">Component1</span></span>  |
| <span data-ttu-id="8fecf-155">FileB</span><span class="sxs-lookup"><span data-stu-id="8fecf-155">FileB</span></span> | <span data-ttu-id="8fecf-156">Component2</span><span class="sxs-lookup"><span data-stu-id="8fecf-156">Component2</span></span>  |
| <span data-ttu-id="8fecf-157">FileC</span><span class="sxs-lookup"><span data-stu-id="8fecf-157">FileC</span></span> | <span data-ttu-id="8fecf-158">Component3</span><span class="sxs-lookup"><span data-stu-id="8fecf-158">Component3</span></span>  |
| <span data-ttu-id="8fecf-159">Arquiva</span><span class="sxs-lookup"><span data-stu-id="8fecf-159">FileD</span></span> | <span data-ttu-id="8fecf-160">Component4</span><span class="sxs-lookup"><span data-stu-id="8fecf-160">Component4</span></span>  |



 

[<span data-ttu-id="8fecf-161">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="8fecf-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="8fecf-162">Diretório</span><span class="sxs-lookup"><span data-stu-id="8fecf-162">Directory</span></span>  | <span data-ttu-id="8fecf-163">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="8fecf-163">Directory\_Parent</span></span> | <span data-ttu-id="8fecf-164">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="8fecf-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="8fecf-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="8fecf-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="8fecf-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="8fecf-166">SourceDir</span></span>  |
| <span data-ttu-id="8fecf-167">Directorya</span><span class="sxs-lookup"><span data-stu-id="8fecf-167">DirectoryA</span></span> | <span data-ttu-id="8fecf-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="8fecf-168">TARGETDIR</span></span>         | <span data-ttu-id="8fecf-169">Directorya</span><span class="sxs-lookup"><span data-stu-id="8fecf-169">DirectoryA</span></span> |



 

<span data-ttu-id="8fecf-170">Para corrigir os erros, reorganize o aplicativo de modo que cada componente contenha apenas recursos por usuário ou por máquina, e não ambos.</span><span class="sxs-lookup"><span data-stu-id="8fecf-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="8fecf-171">A primeira mensagem de erro é postada porque Component1 contém fileA (por máquina) e a chave do Registro HKCU RegKeyA (por usuário).</span><span class="sxs-lookup"><span data-stu-id="8fecf-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fecf-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8fecf-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fecf-173">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="8fecf-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



