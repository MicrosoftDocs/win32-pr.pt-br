---
title: Propriedade RegistrationInfo. Description
description: Para scripts, Obtém ou define a descrição da tarefa.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Agendador de Tarefas de propriedade de descrição
- Propriedade de descrição Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, Propriedade Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369198"
---
# <a name="registrationinfodescription-property"></a><span data-ttu-id="15c1a-106">Propriedade RegistrationInfo. Description</span><span class="sxs-lookup"><span data-stu-id="15c1a-106">RegistrationInfo.Description property</span></span>

<span data-ttu-id="15c1a-107">Para scripts, Obtém ou define a descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="15c1a-107">For scripting, gets or sets the description of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c1a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="15c1a-108">Syntax</span></span>


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a><span data-ttu-id="15c1a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="15c1a-109">Property value</span></span>

<span data-ttu-id="15c1a-110">A descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="15c1a-110">The description of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="15c1a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="15c1a-111">Remarks</span></span>

<span data-ttu-id="15c1a-112">Ao ler ou gravar XML para uma tarefa, a descrição da tarefa é especificada usando o elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="15c1a-112">When reading or writing XML for a task, the description of the task is specified using the [**Description**](taskschedulerschema-description-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="15c1a-113">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="15c1a-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="15c1a-114">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="15c1a-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="15c1a-115">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="15c1a-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="15c1a-116">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="15c1a-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c1a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15c1a-117">Requirements</span></span>



| <span data-ttu-id="15c1a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c1a-118">Requirement</span></span> | <span data-ttu-id="15c1a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="15c1a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15c1a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15c1a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15c1a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15c1a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15c1a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15c1a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15c1a-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15c1a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15c1a-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="15c1a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="15c1a-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15c1a-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15c1a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="15c1a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c1a-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c1a-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c1a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="15c1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c1a-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="15c1a-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





