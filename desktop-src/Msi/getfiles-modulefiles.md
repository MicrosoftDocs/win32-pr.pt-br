---
description: A propriedade ModuleFiles do objeto GetFiles retorna todas as chaves primárias da tabela de arquivos para o módulo aberto no momento.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Propriedade GetFiles. ModuleFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811846"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="6d3c1-103">Propriedade GetFiles. ModuleFiles</span><span class="sxs-lookup"><span data-stu-id="6d3c1-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="6d3c1-104">A propriedade **ModuleFiles** do objeto [**GetFiles**](getfiles-object.md) retorna todas as chaves primárias da [tabela de arquivos](file-table.md) para o módulo aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="6d3c1-105">As chaves primárias são retornadas como uma coleção de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="6d3c1-106">O módulo deve ser aberto por uma chamada para o método [**OpenModule**](merge-openmodule.md) do [objeto de mesclagem](merge-object.md) antes de chamar **ModuleFiles**.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="6d3c1-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3c1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d3c1-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="6d3c1-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d3c1-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6d3c1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d3c1-110">Remarks</span></span>

<span data-ttu-id="6d3c1-111">Observe que a ordem dos arquivos listados na coleção pode não estar na mesma sequência, conforme listado na tabela de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="6d3c1-112">Se o módulo não tiver nenhuma tabela de arquivos ou não contiver nenhum arquivo no idioma específico, ModuleFiles retornará uma coleção vazia de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="6d3c1-113">C++</span><span class="sxs-lookup"><span data-stu-id="6d3c1-113">C++</span></span>

<span data-ttu-id="6d3c1-114">Consulte [**obter \_**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) a função ModuleFiles.</span><span class="sxs-lookup"><span data-stu-id="6d3c1-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3c1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d3c1-115">Requirements</span></span>



| <span data-ttu-id="6d3c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3c1-116">Requirement</span></span> | <span data-ttu-id="6d3c1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6d3c1-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3c1-118">Versão</span><span class="sxs-lookup"><span data-stu-id="6d3c1-118">Version</span></span><br/> | <span data-ttu-id="6d3c1-119">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6d3c1-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6d3c1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d3c1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6d3c1-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c1-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d3c1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6d3c1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d3c1-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c1-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
