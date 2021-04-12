---
description: Crie links simbólicos que usam um caminho absoluto ou relativo usando a função CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Criando links simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297215"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="74dbf-103">Criando links simbólicos</span><span class="sxs-lookup"><span data-stu-id="74dbf-103">Creating Symbolic Links</span></span>

<span data-ttu-id="74dbf-104">A função [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) permite que você crie links simbólicos usando um caminho absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="74dbf-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="74dbf-105">Links simbólicos podem ser links absolutos ou relativos.</span><span class="sxs-lookup"><span data-stu-id="74dbf-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="74dbf-106">Links absolutos são links que especificam cada parte do nome do caminho; os links relativos são determinados em relação ao local em que os especificadores de link estão em um caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="74dbf-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="74dbf-107">Os links relativos são especificados usando as seguintes convenções:</span><span class="sxs-lookup"><span data-stu-id="74dbf-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="74dbf-108">Ponto (.</span><span class="sxs-lookup"><span data-stu-id="74dbf-108">Dot (.</span></span> <span data-ttu-id="74dbf-109">e..) convenções — por exemplo, ".. \\ " resolve o caminho relativo ao diretório pai.</span><span class="sxs-lookup"><span data-stu-id="74dbf-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="74dbf-110">Nomes sem barras ( \) — por exemplo, "tmp" resolvem o caminho relativo ao diretório atual.</span><span class="sxs-lookup"><span data-stu-id="74dbf-110">Names with no slashes (\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="74dbf-111">Relativa à raiz — por exemplo, " \\ Windows \\ System32" resolve para a "*unidade atual*: \\ Windows \\ System32".</span><span class="sxs-lookup"><span data-stu-id="74dbf-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="74dbf-112">directory</span><span class="sxs-lookup"><span data-stu-id="74dbf-112">directory</span></span>
-   <span data-ttu-id="74dbf-113">Diretório de trabalho atual – relativo — por exemplo, se o diretório de trabalho atual for "C: \\ Windows \\ System32", "C:File.txt" será resolvido para "C: \\ Windows \\ System32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="74dbf-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="74dbf-114">**Observação**  Se você especificar um link relativo do diretório de trabalho atual, ele será criado como um link absoluto, devido à maneira como o diretório de trabalho atual é processado com base no usuário e no thread.</span><span class="sxs-lookup"><span data-stu-id="74dbf-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="74dbf-115">Um link simbólico também pode conter pontos de junção e pastas montadas como parte do nome do caminho.</span><span class="sxs-lookup"><span data-stu-id="74dbf-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="74dbf-116">Links simbólicos podem apontar diretamente para um arquivo ou diretório remoto usando o caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="74dbf-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="74dbf-117">Links simbólicos relativos são restritos a um único volume.</span><span class="sxs-lookup"><span data-stu-id="74dbf-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="74dbf-118">Exemplo de um link simbólico absoluto</span><span class="sxs-lookup"><span data-stu-id="74dbf-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="74dbf-119">Neste exemplo, o caminho original contém um componente, '*x*', que é um link simbólico absoluto.</span><span class="sxs-lookup"><span data-stu-id="74dbf-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="74dbf-120">Quando '*x*' é encontrado, o fragmento do caminho original até e incluindo '*x*' é completamente substituído pelo caminho que é apontado por '*x*'.</span><span class="sxs-lookup"><span data-stu-id="74dbf-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="74dbf-121">O restante do caminho depois de '*x*' é anexado a esse novo caminho.</span><span class="sxs-lookup"><span data-stu-id="74dbf-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="74dbf-122">Esse agora se torna o caminho modificado.</span><span class="sxs-lookup"><span data-stu-id="74dbf-122">This now becomes the modified path.</span></span>

<span data-ttu-id="74dbf-123">X: "C: \\ Alpha \\ beta \\ absLink \\ \\ arquivo gama"</span><span class="sxs-lookup"><span data-stu-id="74dbf-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="74dbf-124">Link: "absLink" é mapeado para " \\ \\ machineB \\ share"</span><span class="sxs-lookup"><span data-stu-id="74dbf-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="74dbf-125">Caminho modificado: " \\ \\ machineB \\ compartilhar \\ \\ arquivo gama"</span><span class="sxs-lookup"><span data-stu-id="74dbf-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="74dbf-126">Exemplo de links simbólicos relativos</span><span class="sxs-lookup"><span data-stu-id="74dbf-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="74dbf-127">Neste exemplo, o caminho original contém um componente '*x*', que é um link simbólico relativo.</span><span class="sxs-lookup"><span data-stu-id="74dbf-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="74dbf-128">Quando '*x*' for encontrado, '*x*' será completamente substituído pelo novo fragmento apontado por '*x*'.</span><span class="sxs-lookup"><span data-stu-id="74dbf-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="74dbf-129">O restante do caminho após '*x*' é anexado ao novo caminho.</span><span class="sxs-lookup"><span data-stu-id="74dbf-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="74dbf-130">Todos os pontos (..) neste novo caminho substituem os componentes que aparecem antes dos pontos (..).</span><span class="sxs-lookup"><span data-stu-id="74dbf-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="74dbf-131">Cada conjunto de pontos substitui o componente anterior.</span><span class="sxs-lookup"><span data-stu-id="74dbf-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="74dbf-132">Se o número de pontos (..) exceder o número de componentes, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="74dbf-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="74dbf-133">Caso contrário, quando toda a substituição de componentes for concluída, o caminho final e modificado permanecerá.</span><span class="sxs-lookup"><span data-stu-id="74dbf-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="74dbf-134">X: C: \\ Alpha \\ beta \\ link \\ de \\ arquivo gama</span><span class="sxs-lookup"><span data-stu-id="74dbf-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="74dbf-135">Link: "link" é mapeado para ".. \\ .. \\ teta</span><span class="sxs-lookup"><span data-stu-id="74dbf-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="74dbf-136">Caminho modificado: "C: \\ Alpha \\ beta \\ .. \\ .. \\ \\arquivo gama de teta \\ "</span><span class="sxs-lookup"><span data-stu-id="74dbf-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="74dbf-137">Caminho final: "C: \\ teta \\ gama \\ File"</span><span class="sxs-lookup"><span data-stu-id="74dbf-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="74dbf-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74dbf-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74dbf-139">Links simbólicos</span><span class="sxs-lookup"><span data-stu-id="74dbf-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="74dbf-140">Links físicos e junções</span><span class="sxs-lookup"><span data-stu-id="74dbf-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="74dbf-141">Nomeando arquivos, caminhos e namespaces</span><span class="sxs-lookup"><span data-stu-id="74dbf-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



