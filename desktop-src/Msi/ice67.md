---
description: ICE67 verifica se o destino de um atalho não anunciado pertence ao mesmo componente que o próprio atalho ou se os atributos do componente de destino garantem que ele não altere os locais de instalação.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922465"
---
# <a name="ice67"></a><span data-ttu-id="b44f6-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="b44f6-103">ICE67</span></span>

<span data-ttu-id="b44f6-104">ICE67 verifica se o destino de um atalho não anunciado pertence ao mesmo componente que o próprio atalho ou se os atributos do componente de destino garantem que ele não altere os locais de instalação.</span><span class="sxs-lookup"><span data-stu-id="b44f6-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="b44f6-105">A falha em corrigir um aviso ou erro relatado por ICE67 pode fazer com que o atalho seja inválido se o componente de destino mudar de estado e o componente de origem não tiver.</span><span class="sxs-lookup"><span data-stu-id="b44f6-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="b44f6-106">Por exemplo, quando o componente do arquivo de destino é definido para ser executado da origem, uma reinstalação que altera o componente para resultados locais no componente que contém o atalho que não está sendo reinstalado.</span><span class="sxs-lookup"><span data-stu-id="b44f6-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="b44f6-107">Portanto, o atalho aponta para um local inválido.</span><span class="sxs-lookup"><span data-stu-id="b44f6-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="b44f6-108">Observe que, em alguns casos, o uso de um componente diferente para o atalho é inevitável.</span><span class="sxs-lookup"><span data-stu-id="b44f6-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="b44f6-109">Por exemplo, se o atalho for criado no perfil do usuário e o arquivo for instalado em um diretório sem perfil, talvez você não consiga usar o mesmo componente para ambos os dados.</span><span class="sxs-lookup"><span data-stu-id="b44f6-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="b44f6-110">(Isso resulta em falhas em cenários de vários usuários, como os descritos em [ICE57](ice57.md)).</span><span class="sxs-lookup"><span data-stu-id="b44f6-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="b44f6-111">Nesse caso, você poderá usar atalhos anunciados para obter o comportamento desejado ou pode simplesmente garantir que o componente de destino não possa ser alterado de executar de origem para local.</span><span class="sxs-lookup"><span data-stu-id="b44f6-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="b44f6-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="b44f6-112">Result</span></span>

<span data-ttu-id="b44f6-113">ICE67 retornará um erro ou um aviso se o destino de um atalho não anunciado não pertencer ao mesmo componente que o próprio atalho ou se os atributos do componente de destino não tiverem certeza de que os locais de instalação não serão alterados.</span><span class="sxs-lookup"><span data-stu-id="b44f6-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="b44f6-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b44f6-114">Example</span></span>

<span data-ttu-id="b44f6-115">ICE67 relata o seguinte aviso e erros para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="b44f6-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="b44f6-116">O Shortcut1 é instalado pelo Component2, mas seu arquivo de destino, arquivo1, é instalado pelo Component1.</span><span class="sxs-lookup"><span data-stu-id="b44f6-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="b44f6-117">O componente de destino é marcado como opcional (o que significa que ele pode ser local ou executado da origem).</span><span class="sxs-lookup"><span data-stu-id="b44f6-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="b44f6-118">Uma possível situação que poderia causar um problema é se Component1 muda de execução de origem para local.</span><span class="sxs-lookup"><span data-stu-id="b44f6-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="b44f6-119">Isso faria com que o Shortcut1 apontasse para um local inválido.</span><span class="sxs-lookup"><span data-stu-id="b44f6-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="b44f6-120">Para corrigir esse aviso, instale o atalho como parte de Component1 ou marque Component1 como LocalOnly ou SourceOnly.</span><span class="sxs-lookup"><span data-stu-id="b44f6-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="b44f6-121">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b44f6-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="b44f6-122">Arquivo</span><span class="sxs-lookup"><span data-stu-id="b44f6-122">File</span></span>  | <span data-ttu-id="b44f6-123">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b44f6-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="b44f6-124">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="b44f6-124">File1</span></span> | <span data-ttu-id="b44f6-125">Component1</span><span class="sxs-lookup"><span data-stu-id="b44f6-125">Component1</span></span>  |



 

<span data-ttu-id="b44f6-126">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b44f6-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="b44f6-127">Atalho</span><span class="sxs-lookup"><span data-stu-id="b44f6-127">Shortcut</span></span>  | <span data-ttu-id="b44f6-128">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b44f6-128">Component\_</span></span> | <span data-ttu-id="b44f6-129">Destino</span><span class="sxs-lookup"><span data-stu-id="b44f6-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="b44f6-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="b44f6-130">Shortcut1</span></span> | <span data-ttu-id="b44f6-131">Component2</span><span class="sxs-lookup"><span data-stu-id="b44f6-131">Component2</span></span>  | <span data-ttu-id="b44f6-132">\[\#Arquivo1\]</span><span class="sxs-lookup"><span data-stu-id="b44f6-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="b44f6-133">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b44f6-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="b44f6-134">Componente</span><span class="sxs-lookup"><span data-stu-id="b44f6-134">Component</span></span>  | <span data-ttu-id="b44f6-135">Atributos</span><span class="sxs-lookup"><span data-stu-id="b44f6-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="b44f6-136">Component1</span><span class="sxs-lookup"><span data-stu-id="b44f6-136">Component1</span></span> | <span data-ttu-id="b44f6-137">2</span><span class="sxs-lookup"><span data-stu-id="b44f6-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="b44f6-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b44f6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b44f6-139">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="b44f6-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



