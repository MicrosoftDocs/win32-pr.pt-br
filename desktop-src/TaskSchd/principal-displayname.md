---
title: Propriedade principal. DisplayName
description: Para scripts, Obtém ou define o nome da entidade de segurança..
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Propriedade DisplayName Agendador de Tarefas
- Propriedade DisplayName Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644743"
---
# <a name="principaldisplayname-property"></a><span data-ttu-id="4f69c-106">Propriedade principal. DisplayName</span><span class="sxs-lookup"><span data-stu-id="4f69c-106">Principal.DisplayName property</span></span>

<span data-ttu-id="4f69c-107">Para scripts, Obtém ou define o nome da entidade de segurança..</span><span class="sxs-lookup"><span data-stu-id="4f69c-107">For scripting, gets or sets the name of the principal..</span></span>

## <a name="syntax"></a><span data-ttu-id="4f69c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f69c-108">Syntax</span></span>


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a><span data-ttu-id="4f69c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4f69c-109">Property value</span></span>

<span data-ttu-id="4f69c-110">O nome da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="4f69c-110">The name of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f69c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f69c-111">Remarks</span></span>

<span data-ttu-id="4f69c-112">Ao ler ou gravar XML para uma tarefa, o nome de exibição de uma entidade de segurança é especificado no elemento [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4f69c-112">When reading or writing XML for a task, the display name for a principal is specified in the [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="4f69c-113">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="4f69c-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="4f69c-114">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="4f69c-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="4f69c-115">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="4f69c-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="4f69c-116">Por exemplo, definir esse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="4f69c-116">For example, setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f69c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f69c-117">Requirements</span></span>



| <span data-ttu-id="4f69c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f69c-118">Requirement</span></span> | <span data-ttu-id="4f69c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4f69c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f69c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f69c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f69c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f69c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4f69c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f69c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f69c-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f69c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f69c-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4f69c-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f69c-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f69c-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f69c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4f69c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f69c-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f69c-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f69c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f69c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f69c-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4f69c-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4f69c-130">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="4f69c-130">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





