---
title: Propriedade RegistrationInfo. Author
description: Para scripts, Obtém ou define o autor da tarefa.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Agendador de Tarefas de propriedade de autor
- Propriedade de autor Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, propriedade de autor
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008818"
---
# <a name="registrationinfoauthor-property"></a><span data-ttu-id="f520c-106">Propriedade RegistrationInfo. Author</span><span class="sxs-lookup"><span data-stu-id="f520c-106">RegistrationInfo.Author property</span></span>

<span data-ttu-id="f520c-107">Para scripts, Obtém ou define o autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f520c-107">For scripting, gets or sets the author of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="f520c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f520c-108">Syntax</span></span>


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a><span data-ttu-id="f520c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f520c-109">Property value</span></span>

<span data-ttu-id="f520c-110">O autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f520c-110">The author of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="f520c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f520c-111">Remarks</span></span>

<span data-ttu-id="f520c-112">Ao ler ou gravar XML para uma tarefa, o autor da tarefa é especificado usando o elemento [**autor**](taskschedulerschema-author-registrationinfotype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f520c-112">When reading or writing XML for a task, the task author is specified using the [**Author**](taskschedulerschema-author-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="f520c-113">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="f520c-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="f520c-114">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f520c-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="f520c-115">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="f520c-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="f520c-116">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="f520c-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f520c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f520c-117">Requirements</span></span>



| <span data-ttu-id="f520c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f520c-118">Requirement</span></span> | <span data-ttu-id="f520c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f520c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f520c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f520c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f520c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f520c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f520c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f520c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f520c-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f520c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f520c-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f520c-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f520c-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f520c-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f520c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f520c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f520c-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f520c-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f520c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f520c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f520c-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f520c-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





