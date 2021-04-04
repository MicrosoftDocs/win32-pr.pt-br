---
title: Propriedade TaskFolder. GetFolder
description: Para scripts, obtém uma pasta que contém tarefas em um local especificado.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Agendador de Tarefas de propriedade GetFolder
- Agendador de Tarefas de propriedade GetFolder, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085316"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="6c70c-106">Propriedade TaskFolder. GetFolder</span><span class="sxs-lookup"><span data-stu-id="6c70c-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="6c70c-107">Para scripts, obtém uma pasta que contém tarefas em um local especificado.</span><span class="sxs-lookup"><span data-stu-id="6c70c-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c70c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c70c-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="6c70c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6c70c-109">Property value</span></span>

<span data-ttu-id="6c70c-110">O caminho (local) para a pasta.</span><span class="sxs-lookup"><span data-stu-id="6c70c-110">The path (location) to the folder.</span></span> <span data-ttu-id="6c70c-111">Não use uma barra invertida após o nome da última pasta no caminho.</span><span class="sxs-lookup"><span data-stu-id="6c70c-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="6c70c-112">A pasta de tarefas raiz é especificada com uma barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="6c70c-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="6c70c-113">Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="6c70c-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="6c70c-114">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="6c70c-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="6c70c-115">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="6c70c-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c70c-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6c70c-116">Error codes</span></span>

<span data-ttu-id="6c70c-117">A pasta no local especificado.</span><span class="sxs-lookup"><span data-stu-id="6c70c-117">The folder at the specified location.</span></span> <span data-ttu-id="6c70c-118">A pasta é um objeto [**TaskFolder**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="6c70c-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c70c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c70c-119">Requirements</span></span>



| <span data-ttu-id="6c70c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c70c-120">Requirement</span></span> | <span data-ttu-id="6c70c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6c70c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c70c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c70c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c70c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c70c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6c70c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c70c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c70c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c70c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c70c-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6c70c-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c70c-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c70c-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c70c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6c70c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c70c-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c70c-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





