---
title: Elemento ButtonText
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Elemento ButtonText do Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794504"
---
# <a name="buttontext-element"></a><span data-ttu-id="d3e8d-105">Elemento ButtonText</span><span class="sxs-lookup"><span data-stu-id="d3e8d-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="d3e8d-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d3e8d-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d3e8d-108">O elemento **ButtonText** especifica a cadeia de texto que o Windows Media Player exibe para um botão de painel de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="d3e8d-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3e8d-109">Attributes</span></span>

<span data-ttu-id="d3e8d-110">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d3e8d-111">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="d3e8d-111">Parent/Child Elements</span></span>



| <span data-ttu-id="d3e8d-112">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="d3e8d-112">Hierarchy</span></span>       | <span data-ttu-id="d3e8d-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3e8d-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="d3e8d-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d3e8d-114">Parent elements</span></span> | <span data-ttu-id="d3e8d-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="d3e8d-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="d3e8d-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d3e8d-116">Child elements</span></span>  | <span data-ttu-id="d3e8d-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d3e8d-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="d3e8d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3e8d-118">Remarks</span></span>

<span data-ttu-id="d3e8d-119">Esse elemento é necessário para cada instância de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="d3e8d-120">O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="d3e8d-121">O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="d3e8d-122">O Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas online** . o Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="d3e8d-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="d3e8d-123">O Windows Media Player pode cortar o texto do botão para se ajustar ao espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="d3e8d-124">O Player sempre usa a fonte de 8 pontos em negrito Tahoma para esse texto.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="d3e8d-125">Há duas linhas disponíveis para exibir o texto do botão, mas o Player não quebra automaticamente o texto da primeira linha para a segunda.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="d3e8d-126">Para especificar uma quebra de linha no texto do botão, insira a nova sequência de escape de linha " \\ n" em sua cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="d3e8d-127">A cadeia de texto também é exibida no menu **ir** na interface de usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="d3e8d-128">Você deve testar sua loja online usando uma variedade de configurações de exibição para garantir que o texto seja exibido conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e8d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3e8d-129">Requirements</span></span>



| <span data-ttu-id="d3e8d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e8d-130">Requirement</span></span> | <span data-ttu-id="d3e8d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e8d-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="d3e8d-132">Versão</span><span class="sxs-lookup"><span data-stu-id="d3e8d-132">Version</span></span><br/> | <span data-ttu-id="d3e8d-133">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d3e8d-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3e8d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3e8d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e8d-135">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="d3e8d-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="d3e8d-136">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d3e8d-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="d3e8d-137">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="d3e8d-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





