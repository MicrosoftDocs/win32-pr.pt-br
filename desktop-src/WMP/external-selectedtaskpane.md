---
title: External. SelectedTaskPane
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade SelectedTaskPane especifica ou recupera o painel de tarefas selecionado no momento.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Windows Media Player externo. SelectedTaskPane
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800132"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="62ef0-106">External. SelectedTaskPane</span><span class="sxs-lookup"><span data-stu-id="62ef0-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="62ef0-107">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="62ef0-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="62ef0-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="62ef0-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="62ef0-109">A propriedade **SelectedTaskPane** especifica ou recupera o painel de tarefas selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="62ef0-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ef0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ef0-110">Syntax</span></span>

<span data-ttu-id="62ef0-111">janela. external. SelectedTaskPane = *tarefa*</span><span class="sxs-lookup"><span data-stu-id="62ef0-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="62ef0-112">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="62ef0-112">Possible Values</span></span>

<span data-ttu-id="62ef0-113">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="62ef0-113">This property is a read/write **String**.</span></span> <span data-ttu-id="62ef0-114">Os valores possíveis são "ServiceTask1", "ServiceTask2" e "ServiceTask3".</span><span class="sxs-lookup"><span data-stu-id="62ef0-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="62ef0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="62ef0-115">Remarks</span></span>

<span data-ttu-id="62ef0-116">A especificação de um valor para essa propriedade realça o botão para esse painel.</span><span class="sxs-lookup"><span data-stu-id="62ef0-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="62ef0-117">Ele não torna o painel de tarefas especificado ativo.</span><span class="sxs-lookup"><span data-stu-id="62ef0-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="62ef0-118">Você deve especificar um valor para essa propriedade para definir o botão do painel de tarefas atual para sua página da Web quando a página for carregada para garantir que o botão correto do painel de tarefas esteja ativo.</span><span class="sxs-lookup"><span data-stu-id="62ef0-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="62ef0-119">Para tornar um painel de tarefas específico o ativo, use o método **NavigateTaskPaneURL** .</span><span class="sxs-lookup"><span data-stu-id="62ef0-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ef0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62ef0-120">Requirements</span></span>



| <span data-ttu-id="62ef0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ef0-121">Requirement</span></span> | <span data-ttu-id="62ef0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="62ef0-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62ef0-123">Versão</span><span class="sxs-lookup"><span data-stu-id="62ef0-123">Version</span></span><br/> | <span data-ttu-id="62ef0-124">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="62ef0-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="62ef0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="62ef0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="62ef0-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ef0-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ef0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="62ef0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ef0-128">**Objeto externo para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="62ef0-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="62ef0-129">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="62ef0-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





