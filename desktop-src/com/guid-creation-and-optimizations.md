---
title: Criação e otimizações de GUID
description: Criação e otimizações de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364397"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="3826b-103">Criação e otimizações de GUID</span><span class="sxs-lookup"><span data-stu-id="3826b-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="3826b-104">Como um CLSID, como um IID (identificador de interface), é um GUID, nenhuma outra classe, independentemente de quem o escreve, tem um CLSID duplicado.</span><span class="sxs-lookup"><span data-stu-id="3826b-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="3826b-105">Os implementadores de servidor geralmente obtêm CLSIDs por meio da função [**falha em CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .</span><span class="sxs-lookup"><span data-stu-id="3826b-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="3826b-106">Essa função tem a garantia de produzir CLSIDs exclusivos, portanto, os implementadores de servidor em todo o mundo podem desenvolver e implantar o software de forma independente sem medo de colisão acidental com software escrito por outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="3826b-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="3826b-107">O uso de CLSIDs exclusivos evita a possibilidade de colisões de nome entre classes porque os CLSIDs não estão de maneira alguma conectada aos nomes usados na implementação subjacente.</span><span class="sxs-lookup"><span data-stu-id="3826b-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="3826b-108">Por exemplo, dois fornecedores diferentes podem escrever classes chamadas "StackClass", mas cada uma teria um CLSID exclusivo e, portanto, não poderia ser confundida.</span><span class="sxs-lookup"><span data-stu-id="3826b-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="3826b-109">COM frequência deve mapear GUIDs (IIDs e CLSIDs) para um conjunto arbitrariamente grande de outros valores.</span><span class="sxs-lookup"><span data-stu-id="3826b-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="3826b-110">Como desenvolvedor de aplicativos, você pode ajudar a acelerar essas pesquisas e, assim, melhorar o desempenho do sistema, gerando os GUIDs para seu aplicativo como um bloco de valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="3826b-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="3826b-111">A maneira mais eficiente de gerar um bloco de GUIDs consecutivos é executar o utilitário Uuidgen usando as opções-n e-x, que gera um bloco de UUIDs, cada um deles cujo primeiro valor DWORD é incrementado em um.</span><span class="sxs-lookup"><span data-stu-id="3826b-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="3826b-112">Por exemplo, se você digitar</span><span class="sxs-lookup"><span data-stu-id="3826b-112">For example, if you were to type</span></span>

<span data-ttu-id="3826b-113">**Uuidgen-N5-x**</span><span class="sxs-lookup"><span data-stu-id="3826b-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="3826b-114">o utilitário Uuidgen geraria um bloco de UUIDs semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="3826b-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="3826b-115">Um método para gerar e controlar GUIDs para um projeto inteiro começa com a geração de um bloco de um número arbitrariamente grande de UUIDs, digamos 500.</span><span class="sxs-lookup"><span data-stu-id="3826b-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="3826b-116">Por exemplo, se você digitar</span><span class="sxs-lookup"><span data-stu-id="3826b-116">For example, if you were to type</span></span>

<span data-ttu-id="3826b-117">**Uuidgen-N500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="3826b-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="3826b-118">o utilitário gerará UUIDs consecutivos de 500 e os gravaria no arquivo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="3826b-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="3826b-119">Você pode então verificar esse arquivo em sua árvore de origem, fornecendo um único repositório para todos os GUIDs a serem usados em um projeto.</span><span class="sxs-lookup"><span data-stu-id="3826b-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="3826b-120">À medida que as pessoas exigem GUIDs para suas partes do projeto, eles podem fazer check-out do arquivo, ter vários GUIDs de que precisam, marcá-los como sendo tirados e deixar uma observação sobre onde no código ou "espec" eles estão usando-os.</span><span class="sxs-lookup"><span data-stu-id="3826b-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="3826b-121">Além de melhorar o desempenho do sistema, a geração de blocos de GUIDs consecutivos dessa maneira tem os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="3826b-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="3826b-122">Um arquivo central que contém todos os GUIDs de um aplicativo facilita o controle de quais GUIDs são para o que as pessoas estão usando.</span><span class="sxs-lookup"><span data-stu-id="3826b-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="3826b-123">Um bloco de GUIDs consecutivos associados a um aplicativo específico ajuda os desenvolvedores e testadores a reconhecer GUIDs internos durante a depuração e torna mais fácil encontrá-los no registro do sistema, pois eles são armazenados em sequência.</span><span class="sxs-lookup"><span data-stu-id="3826b-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3826b-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3826b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3826b-125">Responsabilidades do servidor COM</span><span class="sxs-lookup"><span data-stu-id="3826b-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




