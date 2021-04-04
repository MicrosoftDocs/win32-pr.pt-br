---
title: Propriedade MessageBody. defaultmessageaction
description: Para scripts, Obtém ou define o texto da mensagem que é exibido no corpo da caixa de mensagem.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Agendador de Tarefas da propriedade MessageBody
- Propriedade MessageBody Agendador de Tarefas, objeto exmessageaction
- Agendador de Tarefas de objeto MessageBody, propriedade de submensagem
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824252"
---
# <a name="showmessageactionmessagebody-property"></a><span data-ttu-id="b8c4f-106">Propriedade MessageBody. defaultmessageaction</span><span class="sxs-lookup"><span data-stu-id="b8c4f-106">ShowMessageAction.MessageBody property</span></span>

<span data-ttu-id="b8c4f-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-107">\[This object is no longer supported.</span></span> <span data-ttu-id="b8c4f-108">Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.\]</span><span class="sxs-lookup"><span data-stu-id="b8c4f-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="b8c4f-109">Para scripts, Obtém ou define o texto da mensagem que é exibido no corpo da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-109">For scripting, gets or sets the message text that is displayed in the body of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c4f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8c4f-110">Syntax</span></span>


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a><span data-ttu-id="b8c4f-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b8c4f-111">Property value</span></span>

<span data-ttu-id="b8c4f-112">O texto da mensagem que é exibido no corpo da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-112">The message text that is displayed in the body of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c4f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8c4f-113">Remarks</span></span>

<span data-ttu-id="b8c4f-114">Cadeias de caracteres parametrizadas podem ser usadas no texto da mensagem da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-114">Parameterized strings can be used in the message text of the message box.</span></span> <span data-ttu-id="b8c4f-115">Para obter mais informações, consulte a seção de exemplos em [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="b8c4f-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="b8c4f-116">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="b8c4f-117">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="b8c4f-118">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="b8c4f-119">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c4f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8c4f-120">Requirements</span></span>



| <span data-ttu-id="b8c4f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8c4f-121">Requirement</span></span> | <span data-ttu-id="b8c4f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b8c4f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c4f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8c4f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c4f-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8c4f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b8c4f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8c4f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c4f-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8c4f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8c4f-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b8c4f-127">End of client support</span></span><br/>    | <span data-ttu-id="b8c4f-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8c4f-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b8c4f-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b8c4f-129">End of server support</span></span><br/>    | <span data-ttu-id="b8c4f-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8c4f-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b8c4f-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b8c4f-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b8c4f-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b8c4f-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b8c4f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b8c4f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8c4f-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8c4f-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c4f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8c4f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c4f-136">**Permessageaction**</span><span class="sxs-lookup"><span data-stu-id="b8c4f-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

