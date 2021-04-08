---
description: ICE83 valida a tabela MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010907"
---
# <a name="ice83"></a><span data-ttu-id="dffc2-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="dffc2-103">ICE83</span></span>

<span data-ttu-id="dffc2-104">ICE83 valida a [tabela MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="dffc2-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="dffc2-105">Essa ação personalizada de ICE posta um erro se o caminho de chave para um componente que contém um assembly Win32 é definido como o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="dffc2-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="dffc2-106">Explicitamente, o erro será postado se o valor inserido no campo KeyPath da [tabela de componentes](component-table.md) for igual ao valor inserido no \_ campo manifesto do arquivo da tabela MsiAssembly.</span><span class="sxs-lookup"><span data-stu-id="dffc2-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="dffc2-107">Essa ação personalizada de ICE posta um erro se houver pelo menos um registro na tabela MsiAssembly e a [tabela InstallExecuteSequence](installexecutesequence-table.md) não contiver a [ação MsiPublishAssemblies](msipublishassemblies-action.md) e a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="dffc2-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="dffc2-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="dffc2-108">Result</span></span>

<span data-ttu-id="dffc2-109">ICE83 posta os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="dffc2-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="dffc2-110">Erro de ICE83</span><span class="sxs-lookup"><span data-stu-id="dffc2-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="dffc2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dffc2-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffc2-112">O caminho da chave para o assembly do Win32 SxS (componente \_ = \[ 1 \] ) não deve ser seu arquivo de manifesto</span><span class="sxs-lookup"><span data-stu-id="dffc2-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="dffc2-113">ICE83 lança esse erro quando o campo KeyPath de um assembly Win32 é definido como seu arquivo de manifesto (Component. KeyPath = = MsiAssembly. File \_ manifest).</span><span class="sxs-lookup"><span data-stu-id="dffc2-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="dffc2-114">\[1 \] é KeyPath na tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="dffc2-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="dffc2-115">As ações MsiPublishAssemblies e MsiUnpublishAssemblies devem estar presentes na tabela InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="dffc2-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="dffc2-116">ICE83 lança esse erro quando há pelo menos uma entrada na tabela MsiAssembly, mas a tabela InstallExecuteSequence não contém a ação MsiAssemblyPublish e a ação MsiAssemblyUnpublish.</span><span class="sxs-lookup"><span data-stu-id="dffc2-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dffc2-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dffc2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dffc2-118">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="dffc2-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



