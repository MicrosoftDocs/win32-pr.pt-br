---
title: Propriedade RegistrationInfo. Source
description: Para scripts, Obtém ou define de onde a tarefa foi originada. Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Agendador de Tarefas da propriedade de origem
- Propriedade Source Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, Propriedade Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644885"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="5c993-107">Propriedade RegistrationInfo. Source</span><span class="sxs-lookup"><span data-stu-id="5c993-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="5c993-108">Para scripts, Obtém ou define de onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="5c993-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="5c993-109">Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="5c993-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c993-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c993-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="5c993-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5c993-111">Property value</span></span>

<span data-ttu-id="5c993-112">De onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="5c993-112">Where the task originated from.</span></span> <span data-ttu-id="5c993-113">Por exemplo, de um componente, serviço, aplicativo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="5c993-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c993-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c993-114">Remarks</span></span>

<span data-ttu-id="5c993-115">Ao ler ou gravar XML para uma tarefa, as informações de origem da tarefa são especificadas usando o elemento [**Source**](taskschedulerschema-source-registrationinfotype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="5c993-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="5c993-116">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="5c993-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="5c993-117">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="5c993-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="5c993-118">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="5c993-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="5c993-119">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="5c993-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c993-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c993-120">Requirements</span></span>



| <span data-ttu-id="5c993-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c993-121">Requirement</span></span> | <span data-ttu-id="5c993-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5c993-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c993-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c993-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c993-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c993-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5c993-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c993-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c993-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c993-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c993-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5c993-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c993-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c993-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c993-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5c993-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c993-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c993-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c993-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c993-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c993-132">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5c993-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





