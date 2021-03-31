---
title: Propriedadeprovider. title
description: Para scripts, Obtém ou define o título da caixa de mensagem.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Agendador de Tarefas de propriedade de título
- Propriedade Title Agendador de Tarefas, objeto exmessageaction
- Agendador de Tarefas do objeto exmessageaction, Propriedade Title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644425"
---
# <a name="showmessageactiontitle-property"></a><span data-ttu-id="d0f6a-106">Propriedadeprovider. title</span><span class="sxs-lookup"><span data-stu-id="d0f6a-106">ShowMessageAction.Title property</span></span>

<span data-ttu-id="d0f6a-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-107">\[This object is no longer supported.</span></span> <span data-ttu-id="d0f6a-108">Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.\]</span><span class="sxs-lookup"><span data-stu-id="d0f6a-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="d0f6a-109">Para scripts, Obtém ou define o título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-109">For scripting, gets or sets the title of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f6a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0f6a-110">Syntax</span></span>


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a><span data-ttu-id="d0f6a-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d0f6a-111">Property value</span></span>

<span data-ttu-id="d0f6a-112">O título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-112">The title of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f6a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0f6a-113">Remarks</span></span>

<span data-ttu-id="d0f6a-114">Cadeias de caracteres com parâmetros podem ser usadas no texto do título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-114">Parameterized strings can be used in the title text of the message box.</span></span> <span data-ttu-id="d0f6a-115">Para obter mais informações, consulte a seção de exemplos em [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="d0f6a-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="d0f6a-116">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="d0f6a-117">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="d0f6a-118">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="d0f6a-119">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="d0f6a-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f6a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f6a-120">Requirements</span></span>



| <span data-ttu-id="d0f6a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f6a-121">Requirement</span></span> | <span data-ttu-id="d0f6a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d0f6a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f6a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0f6a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f6a-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0f6a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d0f6a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0f6a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f6a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0f6a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0f6a-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d0f6a-127">End of client support</span></span><br/>    | <span data-ttu-id="d0f6a-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0f6a-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="d0f6a-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d0f6a-129">End of server support</span></span><br/>    | <span data-ttu-id="d0f6a-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0f6a-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d0f6a-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d0f6a-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0f6a-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0f6a-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0f6a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f6a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0f6a-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f6a-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f6a-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0f6a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f6a-136">**Permessageaction**</span><span class="sxs-lookup"><span data-stu-id="d0f6a-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

