---
title: Elemento Title (defaultmessagetype)
description: Contém o título da caixa de mensagem.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento de título Agendador de Tarefas
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085278"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="bf116-104">Elemento Title (defaultmessagetype)</span><span class="sxs-lookup"><span data-stu-id="bf116-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="bf116-105">Contém o título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bf116-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="bf116-106">O elemento **title** é definido pelo tipo complexo [**exmessagetype**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bf116-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bf116-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="bf116-107">Parent element</span></span>



| <span data-ttu-id="bf116-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf116-108">Element</span></span>                                                                                  | <span data-ttu-id="bf116-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bf116-109">Derived from</span></span>                                                               | <span data-ttu-id="bf116-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf116-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="bf116-111">**Exmessage (The Action)**</span><span class="sxs-lookup"><span data-stu-id="bf116-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="bf116-112">**defaultmessagetype**</span><span class="sxs-lookup"><span data-stu-id="bf116-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="bf116-113">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bf116-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bf116-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf116-114">Remarks</span></span>

<span data-ttu-id="bf116-115">Para desenvolvimento em C++, consulte a [**Propriedade Title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span><span class="sxs-lookup"><span data-stu-id="bf116-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="bf116-116">Para o desenvolvimento de scripts, consulte o " [**nome do email". título**](showmessageaction-title.md).</span><span class="sxs-lookup"><span data-stu-id="bf116-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf116-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf116-117">Requirements</span></span>



| <span data-ttu-id="bf116-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf116-118">Requirement</span></span> | <span data-ttu-id="bf116-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bf116-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf116-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf116-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf116-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf116-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf116-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf116-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf116-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf116-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





