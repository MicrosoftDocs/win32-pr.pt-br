---
title: Elemento ButtonTip
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Elemento ButtonTip do Windows Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813185"
---
# <a name="buttontip-element"></a><span data-ttu-id="fbe18-105">Elemento ButtonTip</span><span class="sxs-lookup"><span data-stu-id="fbe18-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="fbe18-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="fbe18-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fbe18-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="fbe18-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fbe18-108">O elemento **ButtonTip** especifica a cadeia de caracteres de texto que é exibida quando o usuário aponta para um botão de painel de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fbe18-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="fbe18-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbe18-109">Attributes</span></span>

<span data-ttu-id="fbe18-110">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="fbe18-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="fbe18-111">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="fbe18-111">Parent/Child Elements</span></span>



| <span data-ttu-id="fbe18-112">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="fbe18-112">Hierarchy</span></span>       | <span data-ttu-id="fbe18-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbe18-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="fbe18-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fbe18-114">Parent elements</span></span> | <span data-ttu-id="fbe18-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="fbe18-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="fbe18-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fbe18-116">Child elements</span></span>  | <span data-ttu-id="fbe18-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fbe18-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="fbe18-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbe18-118">Remarks</span></span>

<span data-ttu-id="fbe18-119">Esse elemento é opcional para cada instância de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="fbe18-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="fbe18-120">Se esse elemento não for fornecido, o Windows Media Player usará o texto do botão como o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="fbe18-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="fbe18-121">O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="fbe18-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="fbe18-122">O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fbe18-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="fbe18-123">O Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas online** . o Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="fbe18-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbe18-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe18-124">Requirements</span></span>



| <span data-ttu-id="fbe18-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe18-125">Requirement</span></span> | <span data-ttu-id="fbe18-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fbe18-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="fbe18-127">Versão</span><span class="sxs-lookup"><span data-stu-id="fbe18-127">Version</span></span><br/> | <span data-ttu-id="fbe18-128">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fbe18-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbe18-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbe18-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe18-130">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="fbe18-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="fbe18-131">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="fbe18-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="fbe18-132">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="fbe18-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





