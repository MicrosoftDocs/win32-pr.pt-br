---
description: O ICE62 executa verificações extensivas na tabela IsolatedComponent para dados que podem causar um comportamento inesperado.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768468"
---
# <a name="ice62"></a><span data-ttu-id="14a0a-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="14a0a-103">ICE62</span></span>

<span data-ttu-id="14a0a-104">O ICE62 executa verificações extensivas na [tabela IsolatedComponent](isolatedcomponent-table.md) para dados que podem causar um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="14a0a-105">A falha na correção de um erro relatado pelo ICE62 pode resultar em uma falha do sistema de componentes isolado em uma ampla variedade de formas.</span><span class="sxs-lookup"><span data-stu-id="14a0a-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="14a0a-106">Por exemplo, se o bit SharedDllRefCount não estiver definido para um componente compartilhado, o registro do componente poderá ser removido quando outro aplicativo usar esse ComponentID e for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="14a0a-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="14a0a-107">Result</span></span>

<span data-ttu-id="14a0a-108">ICE62 posta um aviso ou erro quando encontra dados na tabela IsolatedComponent que podem produzir um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="14a0a-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="14a0a-109">Example</span></span>

<span data-ttu-id="14a0a-110">ICE62 relata os erros e avisos a seguir para os exemplos mostrados.</span><span class="sxs-lookup"><span data-stu-id="14a0a-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="14a0a-111">Component2 é listado como o componente de aplicativo para o isolamento de Component1.</span><span class="sxs-lookup"><span data-stu-id="14a0a-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="14a0a-112">No entanto, Component2 tem um caminho de chave do registro e não fornece um caminho executável válido a ser usado para isolar o componente.</span><span class="sxs-lookup"><span data-stu-id="14a0a-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="14a0a-113">Para corrigir esse erro, use um componente diferente como o aplicativo para o componente isolado Component1.</span><span class="sxs-lookup"><span data-stu-id="14a0a-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="14a0a-114">Component1 está listado como um componente compartilhado isolado, mas não tem o conjunto de bits SharedDllRefCount.</span><span class="sxs-lookup"><span data-stu-id="14a0a-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="14a0a-115">Isso pode resultar no tempo de vida do componente estar incorreto.</span><span class="sxs-lookup"><span data-stu-id="14a0a-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="14a0a-116">Se outro aplicativo usar esse componente (isolado ou não) e for desinstalado, o registro do componente será removido, mas a cópia isolada desse aplicativo permanecerá.</span><span class="sxs-lookup"><span data-stu-id="14a0a-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="14a0a-117">Isso causa problemas de reparo e desinstalação.</span><span class="sxs-lookup"><span data-stu-id="14a0a-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="14a0a-118">Para corrigir esse erro, defina o bit SharedDllRefCount para o componente.</span><span class="sxs-lookup"><span data-stu-id="14a0a-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="14a0a-119">Component1 e Component2 são instalados por diferentes recursos.</span><span class="sxs-lookup"><span data-stu-id="14a0a-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="14a0a-120">O Component1 é instalado pelo Feature1 e o Component2 é instalado pelo Feature2.</span><span class="sxs-lookup"><span data-stu-id="14a0a-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="14a0a-121">Feature1 não é pai de Feature2, portanto, é possível que o aplicativo seja instalado, mas não o componente isolado, dividindo o isolamento.</span><span class="sxs-lookup"><span data-stu-id="14a0a-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="14a0a-122">Para corrigir esse erro, adicione uma entrada à tabela FeatureComponents vinculando Component1 ao mesmo recurso que (ou um recurso pai do) o recurso que instala o Component2.</span><span class="sxs-lookup"><span data-stu-id="14a0a-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="14a0a-123">Component1 tem uma condição na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="14a0a-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="14a0a-124">Se essa condição mudar de TRUE para FALSE durante o tempo de vida de uma instalação em um computador, o componente isolado poderá ficar órfão sem informações de registro.</span><span class="sxs-lookup"><span data-stu-id="14a0a-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="14a0a-125">Para corrigir esse aviso, remova a condição ou crie a condição para que ela nunca possa ser alterada de verdadeira para falsa.</span><span class="sxs-lookup"><span data-stu-id="14a0a-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="14a0a-126">Component1 é isolado para Component2 e Component3, e os dois componentes também são instalados no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="14a0a-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="14a0a-127">Os aplicativos compartilham um componente isolado, mas se um aplicativo for removido, o componente compartilhado também será removido, fazendo com que os outros aplicativos percam o componente isolado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="14a0a-128">Para corrigir esse aviso, instale os aplicativos em diretórios diferentes ou verifique se alguns dos aplicativos realmente exigem um componente isolado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="14a0a-129">Tabela IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="14a0a-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="14a0a-130">Componente \_ compartilhado</span><span class="sxs-lookup"><span data-stu-id="14a0a-130">Component\_Shared</span></span> | <span data-ttu-id="14a0a-131">Aplicativo de componente \_</span><span class="sxs-lookup"><span data-stu-id="14a0a-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="14a0a-132">Component1</span><span class="sxs-lookup"><span data-stu-id="14a0a-132">Component1</span></span>        | <span data-ttu-id="14a0a-133">Component2</span><span class="sxs-lookup"><span data-stu-id="14a0a-133">Component2</span></span>             |
| <span data-ttu-id="14a0a-134">Component1</span><span class="sxs-lookup"><span data-stu-id="14a0a-134">Component1</span></span>        | <span data-ttu-id="14a0a-135">Component3</span><span class="sxs-lookup"><span data-stu-id="14a0a-135">Component3</span></span>             |



 

[<span data-ttu-id="14a0a-136">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="14a0a-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="14a0a-137">Componente</span><span class="sxs-lookup"><span data-stu-id="14a0a-137">Component</span></span>  | <span data-ttu-id="14a0a-138">ComponentId</span><span class="sxs-lookup"><span data-stu-id="14a0a-138">ComponentId</span></span> | <span data-ttu-id="14a0a-139">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="14a0a-139">Directory\_</span></span> | <span data-ttu-id="14a0a-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="14a0a-140">Attributes</span></span> | <span data-ttu-id="14a0a-141">Condição</span><span class="sxs-lookup"><span data-stu-id="14a0a-141">Condition</span></span>   | <span data-ttu-id="14a0a-142">KeyPath</span><span class="sxs-lookup"><span data-stu-id="14a0a-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="14a0a-143">Component1</span><span class="sxs-lookup"><span data-stu-id="14a0a-143">Component1</span></span> |             | <span data-ttu-id="14a0a-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="14a0a-144">Dir1</span></span>        | <span data-ttu-id="14a0a-145">0</span><span class="sxs-lookup"><span data-stu-id="14a0a-145">0</span></span>          | <span data-ttu-id="14a0a-146">MyCondition</span><span class="sxs-lookup"><span data-stu-id="14a0a-146">MYCONDITION</span></span> | <span data-ttu-id="14a0a-147">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="14a0a-147">File1</span></span>     |
| <span data-ttu-id="14a0a-148">Component2</span><span class="sxs-lookup"><span data-stu-id="14a0a-148">Component2</span></span> |             | <span data-ttu-id="14a0a-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="14a0a-149">TARGETDIR</span></span>   | <span data-ttu-id="14a0a-150">4</span><span class="sxs-lookup"><span data-stu-id="14a0a-150">4</span></span>          |             | <span data-ttu-id="14a0a-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="14a0a-151">Registry2</span></span> |
| <span data-ttu-id="14a0a-152">Component3</span><span class="sxs-lookup"><span data-stu-id="14a0a-152">Component3</span></span> |             | <span data-ttu-id="14a0a-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="14a0a-153">TARGETDIR</span></span>   | <span data-ttu-id="14a0a-154">0</span><span class="sxs-lookup"><span data-stu-id="14a0a-154">0</span></span>          |             | <span data-ttu-id="14a0a-155">Arquivo3</span><span class="sxs-lookup"><span data-stu-id="14a0a-155">File3</span></span>     |



 

[<span data-ttu-id="14a0a-156">FeatureComponentsTable</span><span class="sxs-lookup"><span data-stu-id="14a0a-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="14a0a-157">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="14a0a-157">Feature\_</span></span> | <span data-ttu-id="14a0a-158">Componente\_</span><span class="sxs-lookup"><span data-stu-id="14a0a-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="14a0a-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="14a0a-159">Feature1</span></span>  | <span data-ttu-id="14a0a-160">Component1</span><span class="sxs-lookup"><span data-stu-id="14a0a-160">Component1</span></span>  |
| <span data-ttu-id="14a0a-161">Feature2</span><span class="sxs-lookup"><span data-stu-id="14a0a-161">Feature2</span></span>  | <span data-ttu-id="14a0a-162">Component2</span><span class="sxs-lookup"><span data-stu-id="14a0a-162">Component2</span></span>  |
| <span data-ttu-id="14a0a-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="14a0a-163">Feature1</span></span>  | <span data-ttu-id="14a0a-164">Component3</span><span class="sxs-lookup"><span data-stu-id="14a0a-164">Component3</span></span>  |



 

<span data-ttu-id="14a0a-165">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="14a0a-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="14a0a-166">Recurso</span><span class="sxs-lookup"><span data-stu-id="14a0a-166">Feature</span></span>  | <span data-ttu-id="14a0a-167">Pai do recurso \_</span><span class="sxs-lookup"><span data-stu-id="14a0a-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="14a0a-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="14a0a-168">Feature1</span></span> |                 |
| <span data-ttu-id="14a0a-169">Feature2</span><span class="sxs-lookup"><span data-stu-id="14a0a-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="14a0a-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14a0a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a0a-171">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="14a0a-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



